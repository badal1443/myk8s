## Why kubeconfig is needed.
#### [kubeconfig](https://kubernetes.io/docs/concepts/configuration/organize-cluster-access-kubeconfig/#:~:text=Use%20kubeconfig%20files%20to%20organize,API%20server%20of%20a%20cluster.) is used to store info such such as cluster name/url, cerificates, users, namespaces etc. This file is used by kubectl command to find certificate details along with cluster name etc to run a command.
  
`kubectl get pods
 --server <https:someclusterserver:6443>
 --client-key <keyname>.key
 --client-certificate <client_cert>.crt
 --certificate-authority <ca>.crt`
