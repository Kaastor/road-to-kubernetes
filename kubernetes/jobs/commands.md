## Jobs

* `kubectl scale job [job-name] --replicas 3` - scaling the job. It increases `parallelism` to 3,
  so another Pod is immediately spun, so three pods are running.
* `kubectl apply -f job-manifest.yaml` - Create Job
* `kubectl delete job basic-job` - Delete Job