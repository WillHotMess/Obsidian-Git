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


# SSH into 172.16.0.4
# Check the status of the Kubelet service (which manages the control plane containers)
sudo systemctl status kubelet

# Check the running control plane containers (kube-apiserver is the critical one)
# Replace 'crictl' with 'docker' or 'podman' if you know your container runtime
sudo crictl ps -a | grep kube-apiserver
