# Namespaces
- Namespaces are a native way to divide a singlr kubernetes cluster into multiple virtual cluster.
- It is like a virtual cluster inside cluster.
- Kubernetes provide 4 namespaces out of the box
    1) default
    2) kebe-node-lease
    3) kube-public
    4) kube-system
## kube-system
- The namespace for object created by Kubernetes system.
## kube-public
- publicely accesible data only read only access.
- A configuremap , which contains the cluster information
## kube-node-lease
- heartbeats of the nodes
- each node has associated lease object in namespace
- these lease object send the heartbeat to the control plane to help if any node is not health it create pod in another healthy node.
## default namespace
- bydefault resource are creating in the default namespace if we are not creat any namespace.

### There are two ways of creating a namespaces
 i) using declerative way
-------------------------------
kubectl create namespaces (namespaces name)

ii) using imperative way
-------------------------

