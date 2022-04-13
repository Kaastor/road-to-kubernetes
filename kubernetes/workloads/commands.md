# Commands

## ReplicationController

* `kubectl scale rc [rc-name] --replicas=10` - Scaling RC. Better way is to change RC config (replicas count)
* `kubectl delete rc [rc-name]` - Deletes RC together with managed Pods
* `kubectl delete rc [rc-name] --cascade=false` - Deletes RC but leaves managed Pods. Handy when we want to change the controller

## Deployment

* `kubectl rollout restart deployment [deployment-name]` - rolling restart of the deployment
