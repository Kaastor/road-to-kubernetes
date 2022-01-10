### General

* `kubectl cluster-info`
* `kubectl get [nodes]`
* `kubectl describe node <node-name>` - detailed information
* `kubectl run kubia --image=luksa/kubia --port=8080 --generator=run/v1` - creates ReplicationController (--generator=run/v1),
  tells that app listens on 8080
* `kubectl expose rc kubia --type=LoadBalancer --name kubia-http` - create a svc o LoadBalancer type to expose
  kubia replicationcontroller to the external world
* `kubectl scale rc kubia --replicas=3` - scale up number of replicas of the pod to three
* `kubectl get pods -o wide` - IP and Node info about the pods
* `kubectl delete all --all` - Delete all resources in current namespace.
* `kubectl edit [object] [object-name]` - Edit object's config

### Labels

Default nodes labels: https://kubernetes.io/docs/reference/labels-annotations-taints/
