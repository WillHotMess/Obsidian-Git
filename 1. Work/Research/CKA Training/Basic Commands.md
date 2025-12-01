Here is a list of low-risk, beginner-friendly kubectl commands that help you interact with and explore your Kubernetes cluster without making changes to resources. These are ideal for understanding your environment and viewing basic cluster information.[1][2][3][5]

### Basic Cluster Information

- `kubectl cluster-info`  
  Displays cluster endpoint information and confirms cluster access.[2]

- `kubectl config current-context`  
  Shows which Kubernetes cluster (context) is currently active.[3][2]

- `kubectl config get-contexts`  
  Lists all cluster contexts you can access.[2][3]

- `kubectl config use-context <context-name>`  
  Switches between clusters, if your kubeconfig lists multiple clusters.[3][2]

### Viewing Namespaces

- `kubectl get namespaces`  
  Lists all namespaces in your cluster.[5]

### Viewing Nodes

- `kubectl get nodes`  
  Lists all nodes (machines) in your cluster.[4]

### Viewing Pods

- `kubectl get pods`  
  Lists all pods in the current namespace.[6][2]

- `kubectl get pods -n <namespace>`  
  Lists pods in a specific namespace.[2]

- `kubectl get pods --all-namespaces` or `kubectl get pods -A`  
  Lists pods across all namespaces.[6]

- `kubectl describe pod <pod-name>`  
  Gives detailed information about a particular pod.[6][2]

### Viewing Services and Other Resources

- `kubectl get services`  
  Lists all services in the current namespace.[9]

- `kubectl get all`  
  Lists all resource types (pods, services, deployments, etc.) in the current namespace.[6]

### Exploring Resource Details

- `kubectl describe <resource> <name>`  
  Shows detailed configuration and state for any resource (e.g. `kubectl describe node <node-name>` or `kubectl describe service <service-name>`).[2][6]

### Viewing Logs

- `kubectl logs <pod-name>`  
  Displays running logs from a specified pod.[2]

***
Tearing down a Kubernetes cluster provisioned with kubeadm requires performing two main steps on each node: draining the node and then executing the kubeadm reset command.
The kubeadm reset command performs a best-effort revert of all changes made by kubeadm init or kubeadm join on the host.
💥 Tear Down Steps
You must run these commands on each node in your cluster, starting with the worker nodes and finishing with the control plane (master) node.
Step 1: Drain and Delete Worker Nodes (Run on the Control Plane)
For every worker node you wish to remove, you must first tell the control plane to empty the node of all running pods.
 * Drain the Node: Run the following command from your Control Plane Node (where you have a working kubectl configuration).
   # Replace <node-name> with the actual name of your worker node
kubectl drain <node-name> --ignore-daemonsets --delete-emptydir-data --force

   * --ignore-daemonsets: Ignores pods managed by DaemonSets, as they will be recreated elsewhere.
   * --delete-emptydir-data: Required if the node hosts any pods with EmptyDir volumes.
   * --force: Required to force the removal of pods that are not backed by a controller.
 * Delete the Node Object: After draining, remove the node object from the cluster state.
   kubectl delete node <node-name>

Step 2: Reset the Node (Run on the Node being Removed)
Once a node has been drained and removed from the cluster object store, you need to clean up its local components.
 * Execute kubeadm reset: Run this command on the actual machine you are removing (the worker node, then finally the control plane node).
   # Run this on the worker node first, then the control plane node
sudo kubeadm reset

   * Note: If you are tearing down the last Control Plane Node, the reset will remove the local etcd member data, effectively destroying the cluster's data store.
Step 3: Clean Up Leftover Files and Networking (Run on all Nodes)
The kubeadm reset command intentionally leaves some items behind, particularly networking rules and local Kubernetes configuration files.
 * Clear iptables Rules: Flush all iptables rules created by kube-proxy. This is important to ensure a clean start if you plan to reuse the node for a new cluster.
   sudo iptables -F && sudo iptables -t nat -F && sudo iptables -t mangle -F && sudo iptables -X

 * Remove CNI Configuration: Delete the CNI networking configuration files.
   sudo rm -rf /etc/cni/net.d

 * Remove kubeconfig (Optional, on your client/user machine): If you ran kubeadm init, you copied the admin configuration to your user's home directory. Remove this to avoid stale configuration.
   rm -rf $HOME/.kube

> 💡 For a Single-Node Cluster (like a lab environment): You can skip Step 1 and proceed directly to Steps 2 and 3 on the single control plane machine.
> 
