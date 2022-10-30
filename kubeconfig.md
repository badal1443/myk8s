# Why kubeconfig is needed.
#### [kubeconfig](https://kubernetes.io/docs/concepts/configuration/organize-cluster-access-kubeconfig/#:~:text=Use%20kubeconfig%20files%20to%20organize,API%20server%20of%20a%20cluster.) is used to store info such such as cluster name/url, cerificates, users, namespaces etc. This file is used by kubectl command to find certificate details along with cluster name etc to run a command.
  
`kubectl get pods
 --server <https:someclusterserver:6443>
 --client-key <keyname>.key
 --client-certificate <client_cert>.crt
 --certificate-authority <ca>.crt`
 
 ### Instead of typing this long command above we can have these options inside config file and use following command.
 
 `kubeconfig get pods --kubeconfig config file location`
 
 > this config file is stored in 1 hidden directory inside home directory of user e.g. 
 > ~/.kube/config

If config file is  `$HOME/.kube/config` no need to provide it as an argument to kubectl command. Use:

`kubectl get pod`

> This config file is in YAML, but we never create this as a kubernetes object.


#### Command to view default config file
> kubectl config view

#### Command to view specific config file
> kubectl config view --kubeconfig=path to config file

#### Change the context of kubeconfig to use another cluster.
> kubectl config use-context username@clustername
  
