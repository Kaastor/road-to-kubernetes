## Namespaces
* Labels can overlap, so often we could have overlapping groups of Pods.
  Namespaces are the solution to have non-overlapping groups.
    * **If several users or groups of users are using the same Kubernetes
      cluster, and they each manage their own distinct set of resources, they should each use
      their own namespace.** Can be also used for permissions set up.
    * We would want to keep separate names for different projects in the Organization. If several
    * From the beginning all Pods and other objects are created in `default` namespace. There also exist i.e. `kube-system`
      namespace which holds K8 specific Pods.
* **Be careful:** **namespaces** to not guarantee resources isolation. Pods could be communicating with each other even if they are in separate namespaces.
  Whether namespaces provide network isolation depends on which networking solution is deployed with Kubernetes.

