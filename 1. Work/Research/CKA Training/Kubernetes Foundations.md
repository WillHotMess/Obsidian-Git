
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
	- Engages / Monitors API
- Kube-proxy
	- Network
	- Engages / Monitors API
- Container Runtime
	- Container-D 
	- Docker

