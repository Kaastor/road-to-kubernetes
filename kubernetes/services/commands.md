# Commands

## Service
* `kubectl exec kubia-rc-2bbsv -- env` - Show environment variables available inside the container 
* `gcloud compute firewall-rules create kubia-svc-rule --allow=tcp:30123` - Allow external connections to nodes on port 30123