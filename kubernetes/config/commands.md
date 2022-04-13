### Context

* `kubectl config set-context dev 
  --namespace=[namespace] 
  --cluster=[cluster-name]
  --user=[user-name]` - create contexts for specific namespace
* `kubectx [ctx-name]` - change context to `ctx-name`

### Watch

* `sudo docker run --rm -it -v ~/.kube/config:/root/.kube/config quay.io/derailed/k9s` - app for live k8s watch
