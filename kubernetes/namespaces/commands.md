### Namespaces

* `kubectl get ns` - Get all Namespaces
* `kubectl create -f custom-namespace.yaml` - Create Namespace from YAML
* `kubectl create namespace custom-namespace` - Create namespace from command
* `kubectl get po --namespace kube-system` - Get all Pods in Namespace. If --ns not specified then K8 returns objects from ns set up in `current context`
* `kubectl create -f kubia-manual.yaml -n custom-namespace` - Create an object under namespace
* `alias kcd='kubectl config set-context $(kubectl config current-context) --namespace'` - Quickly switch to a different namespace, by setting up the following
  alias. Usage: `kcd some-namespace`
* `kubectl delete ns custom-namespace` - Delete namespace. Along with it will be deleted all it's resources.
* `kubectl delete all --all` - Delete all resources in current namespace. 
