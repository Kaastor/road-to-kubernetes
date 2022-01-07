## Docker

* `docker run --name kubia-container -p 8080:8080 -d kubia` - run a new containter with name 'kubia-container', 
  map port 8080 from local to container 8080, use 'kubia' image
* `docker inspect [container-name]` - container information
* `docker exec -it kubia-container bash` - log into the container
* `docker stop [container-name]` 
* `docker em [container-name]` 


## Kubernetes

* `kubectl cluster-info`
* `kubectl get [nodes]`
* `kubectl describe node <node-name>` - detailed information
* `kubectl run kubia --image=luksa/kubia --port=8080 --generator=run/v1` - creates ReplicationController (--generator=run/v1),
tells that app listens on 8080
* `kubectl expose rc kubia --type=LoadBalancer --name kubia-http` - create a svc o LoadBalancer type to expose
 kubia replicationcontroller to the external world
* `kubectl scale rc kubia --replicas=3` - scale up number of replicas of the pod to three
* `kubectl get pods -o wide` - IP and Node info about the pods

### Labels

Default nodes labels: https://kubernetes.io/docs/reference/labels-annotations-taints/

## GCP

* `gcloud compute ssh <node-name>` - log into the GCP node

## Minikube

* `minikube start`
