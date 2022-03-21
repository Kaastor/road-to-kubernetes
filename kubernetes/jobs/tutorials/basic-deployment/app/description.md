## Description

* Create an app to invoke K8 Jobs on request
* Use python k8 API - `https://github.com/kubernetes-client/python`
* Create a Docker image that runs the script (`Dockerfile`)
  * `docker build -t przomys/python-k8-job .` 
  * `docker image push przomys/python-k8-job` 
* Create a **Kubernetes Service Account**, **Role**, and **RoleBinding** to give to the Pod the job creation/deletion 
  permission (and deploy them on Kubernetes) ([tutorial](https://blog.meain.io/2019/accessing-kubernetes-api-from-pod/))
* Create a Pod running the Docker container (and deploy it on Kubernetes)