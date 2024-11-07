-->  kubectl create namespace (namespace name)  (to create namespace using kubectl way)

--> kubectl apply -f filename.yaml (after creating .yaml file and .yml file we can apply it is the declerative way of creating namespace)

--> kubectl get namespaces (to get all the namespaces)

--> kubectl get all (to get all the resources present in the default namespaces)

--> kubectl get -n (namespace name) (to get particular namespace resources)

--> kubectl get all -all-namespaces  or kubectl get all -A (to get all the resources of the all namespaces)

--> kubectl config set-context --current --namespace=<namespace name> (to change bydefault namespace to particular namespace)

--> kubectl delete (namespcae name) (delete the namespace if the namespace is delete the all the resource of the namespace is delete)
