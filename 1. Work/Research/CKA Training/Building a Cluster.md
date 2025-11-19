

## Control Plane Node

### Certificate Authority
- Self signed CA
	- Can be part of an external PKI
- Secures cluster communications
- API server 
- Auth of Users and Cluster components 
stored in ``/etc/kubernetes/pki
https://kubernetes.io/docs/reference/setup-tools/kubeadm/kubeadm-init/

### kubeadm Created kubeconfig Files
- Used to define how to connect to your cluster
	- Client certificates 
	- Cluster API Server network location 
- admin.conf
- super-admin.conf
- controller-manager.conf
- scheduler.conf
- kubelet.conf 

### Static Pod Manifests
- Manifest describes a configuration
	- ``/etc/kubernetes/manifests
	- etcd
	- API Server
	- Controller Manager
	- Scheduler
- Watched by the kubelet started automatically when the systems starts

### Pod Networking
- Single un NATed IP address per Pod
	- Direct routing
	- Configures infra to support IP reachability between pods and nodes
- Overlay networking
	- Software defined layer 3
		- Flannel: layer 3 vnet
		- Calico: L3 and policy based traffic management
		- Weave Net: multi-host network

## Creating a Control Plane Node
wget https://raw.githubusercontent.com/projectcalico/calico/master/manifests/calico.yaml




