```
* A statefulSet runs a group of pods , and maintains a stick identity for each of those pods , This is useful for managing applications that neede persistent storage or a stable unique network identity.

* A Deployment manages a set of pods to run an application workload , usually one that does not maintain state.

* ReplicaSet ensure that a specified number of pod replicas are running at one time.

* A controller that watches the shared state of the cluster through the api server and makes changes attempting to move the current state towards the desired state.

* spec.template an spec.selector are only the only required files in the spec.

* .spec.selector is immutable after creatiom of the Deployment.

* spec.selector must match .spec.template.metadata.labels , or else it is rejected by the API.

* spec.replicas is a optional field bydefault it is 1.

* .spec.selector is a required field that specifies a label slector for the pods targeted by the deployment.

*  .spec.strategy specifies the strategy use to replace old pods by new pods , .spec.strategy.type can be "recreate " or "RollingUpdate"  and "RollingUpdate" is the default value.

Recreate Deployment --> All the existing Pods are killed before new ones are created when .spec.strategy.type==Recreate.

Rolling Update Deployment
maxUnavailable
--------------------
 It is an optional fields that specifies the maximum number of pods that can be unavilable during the update process.

Max Surge
-------------
--> It is an optional field that specifies the maximum number pods that can be created over the desired number of pods.

-->  The pod-template-hash label is added by the deployment controller to every replicaSet that the deployment creates.
```
--> kubectl get deployments

--> kubectl rollout status deployment/<deployment-name> (To see the deployment rollout status)

--> kubectl get pods --show-labels  (to see the labels automatically generated for each pod)

--> kubectl get deployment nginx-deployment
```
 ### Upating A deployment
```
--> Deployment ensure that only certain number of pods are down while they are being update  , By default it ensures that at least 75% of the desired number of pods are up (25% max surge).

--> Deployment also ensure that only certain number of pods are created above the desire number of pods , BY default it ensure that at most 125% of the desired number are up.
```
```
--> kubectl set image deployment/nginx-deployment <container_name>=<update_version>

--> kubectl describe deployments.

--> kubectl rollout history dployment/<deployment-name>

--> kubectl rollout undo deployment/nginx-deployment

--> kubectl rollout history deployment/<deployment-name> --revision=2

--> Kubectl rollout undo deployment/<deployment-name> --to-revision=2

--> kubectl scale deployment/nginx-deployment --replicas=10
```
