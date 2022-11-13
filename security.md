
## RBAC 

Steps:
 > Create Role
 > Create RoleBaindings

UseFul Commands:
Check is I have access for certain access in default namespace.
> kubectl auth can-i delete pod

As admin check if another user has certain access
> kubectl auth can-i delete pod --as dev-user
