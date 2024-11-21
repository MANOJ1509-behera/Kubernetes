# Kubernetes

### 50 most important Kubernetes Commands
```
Basic Operations
✔️ `kubectl get pods` - List all pods in the current namespace
✔️ `kubectl get pods -A` - List pods across all namespaces
✔️ `kubectl get pods -o wide` - List pods with more detailed information
✔️ `kubectl get nodes` - List all nodes in the cluster
✔️ `kubectl describe node <node-name>` - Show detailed node information

Pod Management
✔️ `kubectl describe pod <pod-name>` - View detailed pod information
✔️ `kubectl logs <pod-name>` - Fetch pod logs
✔️ `kubectl logs -f <pod-name>` - Stream pod logs in real-time
✔️ `kubectl exec -it <pod-name> -- /bin/bash` - Open shell in pod
✔️ `kubectl port-forward <pod-name> 8080:80` - Forward local port to pod

Deployment Operations
✔️ `kubectl get deployments` - List all deployments
✔️ `kubectl rollout history deployment <name>` - View deployment history
✔️ `kubectl rollout undo deployment <name>` - Rollback to previous version
✔️ `kubectl scale deployment <name> --replicas=5` - Scale deployment
✔️ `kubectl set image deployment/<name> container=image:tag` - Update container image

Configuration & Security
✔️ `kubectl get configmaps` - List all ConfigMaps
✔️ `kubectl get secrets` - List all Secrets
✔️ `kubectl create secret generic <name> --from-file=./file` - Create secret from file
✔️ `kubectl create configmap <name> --from-env-file=.env` - Create ConfigMap from env file
✔️ `kubectl get serviceaccounts` - List service accounts

Namespace Management
✔️ `kubectl get namespaces` - List all namespaces
✔️ `kubectl create namespace <name>` - Create namespace
✔️ `kubectl delete namespace <name>` - Delete namespace
✔️ `kubectl config set-context --current --namespace=<name>` - Switch namespace
✔️ `kubectl get quota --all-namespaces` - Show resource quotas

Service & Networking
✔️ `kubectl get services` - List all services
✔️ `kubectl get endpoints` - List service endpoints
✔️ `kubectl get ingress` - List all ingress rules
✔️ `kubectl describe ingress <name>` - Show ingress details
✔️ `kubectl get networkpolicies` - List network policies

Storage Operations
✔️ `kubectl get pv` - List persistent volumes
✔️ `kubectl get pvc` - List persistent volume claims
✔️ `kubectl describe pv <name>` - Show volume details
✔️ `kubectl describe pvc <name>` - Show volume claim details
✔️ `kubectl get storageclasses` - List storage classes

Cluster Management
✔️ `kubectl cluster-info` - Display cluster information
✔️ `kubectl top nodes` - Show node resource usage
✔️ `kubectl top pods` - Show pod resource usage
✔️ `kubectl api-resources` - List all resources
✔️ `kubectl get events --sort-by=.metadata.creationTimestamp` - Show sorted events
```
