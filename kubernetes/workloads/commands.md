# Commands

## ReplicationController

* `kubectl scale rc [rc-name] --replicas=10` - Scaling RC. Better way is to change RC config (replicas count)
* `kubectl delete rc [rc-name]` - Deletes RC together with managed Pods
* `kubectl delete rc [rc-name] --cascade=false` - Deletes RC but leaves managed Pods. Handy when we want to change the controller

## Jobs

* `kubectl scale job [job-name] --replicas 3` - scaling the job. It increases `parallelism` to 3, 
  so another Pod is immediately spun, so three pods are running.