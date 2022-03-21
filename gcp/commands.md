## GCP

* `export my_zone=us-central1-a`
  
  `export my_cluster=standard-cluster-1` - set the environment variable for the zone and cluster name
* `gcloud compute ssh <node-name>` - log into the GCP node
* `gcloud compute firewall-rules create kubia-svc-rule --allow=tcp:30123` - Allow external connections to nodes on port 30123
* `source <(kubectl completion bash)` - configure kubectl tab completion in Cloud Shell
* `gcloud container clusters get-credentials $my_cluster --zone $my_zone` - configure access to your cluster for the kubectl command-line tool


