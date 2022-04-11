## ConfigMap

* ` kubectl patch cm source-cm -p '{"metadata":{ "name":"target-cm"}}' --dry-run=client -o yaml | kubectl apply -f -
  ` - copy a configmap but with another name in the same namespace