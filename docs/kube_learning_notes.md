
# https://kubernetes.io/docs/tutorials/kubernetes-basics/explore/explore-intro/

## Kubernetes Pods
Pods are the atomic unit on the Kubernetes platform. When we create a Deployment on Kubernetes, that Deployment creates Pods with containers inside them (as opposed to creating containers directly). Each Pod is tied to the Node where it is scheduled, and remains there until termination (according to restart policy) or deletion. In case of a node failure, identical pods are scheduled on other available Nodes in the cluster.


## Nodes

A Pod always runs on a Node. A Node is a worker machine in Kubernetes and may be either a virtual or a physical machine, 
depending on the cluster. Each Node is managed by the Master. A Node can have multiple pods, and the Kubernetes master 
automatically handles scheduling the pods across the Nodes in the cluster. The Master's automatic scheduling takes 
into account the available resources on each Node.

## Every Kubernetes Node runs at least:
  Kubelet, a process responsible for communication between the Kubernetes Master and the Node; 
  it manages the Pods and the containers running on a machine.
  
  A container runtime (like Docker, rkt) responsible for pulling the container image from a registry, 
  unpacking the container, and running the application.
