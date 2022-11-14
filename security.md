
## RBAC 

Steps:
 > Create Role
 > Create RoleBaindings


Checking kube-apiserver setting on master node
check following file
> /etc/kubernetes/manifests/kube-apiserver.yaml

UseFul Commands:
Check is I have access for certain access in default namespace.
> kubectl auth can-i delete pod

As admin check if another user has certain access
> kubectl auth can-i delete pod --as dev-user
