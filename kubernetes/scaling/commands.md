## Autoscaling

* `kubectl autoscale deployment [deployment-name] --cpu-percent=30 --min=1 --max=5` - creates the HPA object for you and sets the Deployment called kubia as the scal-
  ing target. You’re setting the target CPU utilization of the pods to 30% and specifying the minimum and maximum number of replicas.
  * `--cpu-percent=30` - The target average CPU utilization (represented as a percent of requested CPU) over all the pods.
* `kubectl get hpa.v2beta1.autoscaling [deployment-name] -o yaml` - definition of the `HorizontalPodAutoscaler` resource
* `kubectl edit hpa [name]` - edit `targetAverageUtilization`

## Testing & Debugging
* `watch -n 1 kubectl get hpa,deployment` - watching multiple resources in parallel. hpa,deployment - comma separated resources
* `kubectl run -it --rm --restart=Never loadgenerator --image=busybox -- sh -c "while true; do wget -O - -q http://kubia.[namespace]; done"` -
  pod hitting `kubia` service, will kill the process as soon as CTRL+C is pressed. `--restart=Never` option causes kubectl run to create an unman-
  aged pod directly.
  
## Cluster Autoscaling
* `gcloud container clusters update [cluster-name] --enable-autoscaling --min-nodes=3 --max-nodes=5` - enable the Cluster Autoscaler
* `kubectl cordon <node>` - marks the node as unschedulable (but doesn’t do anything with pods running on that node)
* `kubectl drain <node>` - marks the node as unschedulable and then evicts all the pods from the node




