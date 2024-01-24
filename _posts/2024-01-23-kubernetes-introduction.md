Kubernetes is an opensource container orchestration platform. It automates the deployment, scaling and management (app infra, compute and storage) of containerized applications. Google used a proprietary container orchestration system called borg back in 2003-2004. This system managed the deployment of thousands of applications within google. Later in 2014 google opensourced it with the name kubernetes

## Kubernetes Cluster 
K8s cluster includes a group of machines called nodes. Nodes contain pods. Pods have one or more containers
![image](/assets/images/k8s-cluster.png)

There are two core pieces in a kubernetes cluster  

### I. Control Plane
It is responsible for managing the state of the cluster. In production envs the control plane runs on multiple nodes that span across several data center zones. It has

1. Controller manager
  - It is responsible for running controllers that manage the state of various resources in the cluster. E.g.
    - Replication controller - responsible for maintaining the desired replica of the pods
    - Deployment controller - responsible for rolling update and rolling back of deployment
  - The Controller Manager continuously monitors the state of kubernetes resources and takes corrective actions to bring them (aka cluster) to its desired state. 

2. Scheduler
  - It is responsible for scheduling pods onto the worker nodes. It decides based on the resources required by the pod and the resources available on the worker node to schedule the pod

3. etcd
  - It is a distributed key value store. It stores cluster’s persistent state. It is used by other three components: controller manager, scheduler and api server to store and retrieve information about the cluster

4. API server 
  - It is the interface between control plane and data plane  

![image](/assets/images/k8s-architecture.png)

### II. Set of worker nodes
These nodes run the containerized application workloads. Containerized workloads run in pods. Pods are the smallest deployable units in kubernetes. Pod hosts one or more containers and provides shared storage and networking for those containers. Pods are created and managed by kubernetes control plane. Components of worker nodes

1. Kubelet
  - It is a daemon that runs on each worker node. It receives info from API server and maintains the desired state of the pod

2. Container run time
  - It runs the containers on the worker nodes. It is responsible for pulling the container images from registry, starting and stopping the containers, and managing the container resources

3. Kube-proxy
  - It is a networking proxy that runs on each nodes. It is responsible for routing traffic to the correct pods. It also provides load balancing to the pods and ensures the traffic is evenly distributed across the pods



