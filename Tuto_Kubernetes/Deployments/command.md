```
--> kubectl get deployments

--> kubectl rollout status deployment/<deployment-name> (To see the deployment rollout status)

--> kubectl get pods --show-labels  (to see the labels automatically generated for each pod)

--> kubectl get deployment nginx-deployment

--> kubectl set image deployment/nginx-deployment <container_name>=<update_version>

--> kubectl describe deployments.

--> kubectl rollout history dployment/<deployment-name>

--> kubectl rollout undo deployment/nginx-deployment

--> kubectl rollout history deployment/<deployment-name> --revision=2

--> Kubectl rollout undo deployment/<deployment-name> --to-revision=2

--> kubectl scale deployment/nginx-deployment --replicas=10

```
