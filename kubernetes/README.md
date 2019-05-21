# Kubernetes

- Kubernetes is an open source system for managing containerized applications across multiple hosts
- kubernetes : https://github.com/kubernetes/kubernetes

##### Basic Concept

###### Hardware

- Nodes:  A node is the smallest unit of computing hardware in kubernetes e.g. Physical Machine in datacenter.
- The Cluster : The Kubernetes way, Nodes pool together their resources ( RAM and CPU ) to form a more powerful machine called Cluster. "Borg" Concept.
- Persistent Volumes : To store data permanently, Kubernetes uses Persistent Volumes. Mounted to the cluster without being associated with any node. 

###### Software

- Containers : Programs running on Kubernetes are packaged as seft-contained Linux execution environments called Containers.
- Pods : Kubernetes doesn't run containers directly,  instead it wraps one or more containers into a higer-level structure called a pod. 

###### Deployments

- Pods are the basic unit but they are managed by one more layer of abstraction : the deployment
- Main Tasks: When deployment added to cluster it decide how many replicas of a pod to run, it monitor them, if a pod dies, re-create it.

###### Ingress

- Kubernetes provides isolation between pods and the outside world. If you want to communicate with a service running in a pod, you have to open up a channel for communication. This is referred to as ingress. 
- 1. Ingress controller
- 2. LoadBalancer


##### Other links

- LIghtweight Kubernetes : https://github.com/rancher/k3s
- K3s : https://k3s.io/


##### Refrences
- [Kubernetes 101: Pods, Nodes, Containers, and Clusters ](https://medium.com/google-cloud/kubernetes-101-pods-nodes-containers-and-clusters-c1509e409e16)
