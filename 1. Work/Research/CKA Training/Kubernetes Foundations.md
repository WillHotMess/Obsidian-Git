
# What is K8s?
How does K8s add persistency to all the ephemerality? 
- Services
	- Networking abstractions for Pod access
	- IP & DNA names for the Service
	- Dynamically updated based on Pod lifecycle
	- Scaled by adding/removing pods
	- Load balancing

Where is data stored? 
- Persistent Volumes 
	- In the Pod's definition, it makes a "claim" for storage needed


# K8s Architecture

## Cluster Components
### Control Plane Node 
- Primary access point 
- Made up of 
	- API Server (Stateless)
	- ETCD (coded state)
	- Scheduler ()
	- Controller Manager (monitors desired state)
- Use ``kubectl`` for engaging 

#### API Server
- Central 
- Simple 
- RESTful
- Updates etcd

### Node
- Node start/maintain the containers
- Contributes to resources needed
- Virtual or Physical Machines
#### Components
The following services run on all Nodes: 
- Kubelet 
	- Monitors API server for changes
	- Responsible for Pod Lifecycle
	- Reports Node & Pod state
	- Pod probes
	- Engages / Monitors API
- Kube-proxy
	- Network
	- iptables
	- Implement Service 
	- Routing traffic to Pods
	- Load Balancing
- Container Runtime
	- Downloads images & run containers
	- CRI (Container Runtime Interface)
	- containerd is standard (OOTB)
		- Docker used to be the standard

The following are add-ons:
- DNS 
- Ingress controller
	- Layer 7 load balancers 



7dfda10db30de48d2c5c05242c0c3b1ac65c2542c0e49d774a3742fb4ae51004
172.31.24.10 172.17.0.1 fe80::10dd:37ff:fec8:6bf1
