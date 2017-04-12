# k8s
Cluster is deployed on ubuntu 16.10 via kubeadm (current 1.6)
https://kubernetes.io/docs/getting-started-guides/kubeadm/

IngressController (trafik) is deployed via DaemonSet.
https is work in progress

SDS is not implemented yet

RBAC is implemented too permissive via:
https://github.com/ben-st/k8s/blob/master/RBAC/permissive-service-accounts
i will fix this in the near future with correct service accounts

You can try via the hello-world app if everything is setup correctly.

Steps you need to accomplish in order for this to work:
- get an a record for the hello-world app e.g. hello.foo.bar
- Change the domain in the hello deployment file to your domain e.g. hello.foo.bar
- browse to the domain or use curl e.g. `curl hello.foo.bar`
- check your firewall/selinux policy if something is not working correctly
