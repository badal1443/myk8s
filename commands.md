Command Name

purpose

result

Kubectl version

kubectl config view

kubectl config view

apiVersion: v1

clusters: null

contexts: null

current-context: ""

kind: Config

preferences: {}

users: null

kubectl config set-cluster <cluster-name> --server=127.0.0.1:8087

kubectl config get-clusters

kubectl config set-credentials username --token=ers345hf…

kubectl config set-credentials username --username=user1 --password==pwd

kubectl config set-credentials username --client-certificate=my-certificate .crt  --client-key=my-key.key

kubectl config get-users

kubectl config context this-context--cluster=my-cluster --user=my-user

kubectl config set-context this-context --cluster=my-cluster --user=my-user --namespace=qa_env

kubectl config use-context mycontext

kubectl config get-contexts

resource commands, “kubetctl get”

kubectl get pods

displays all pods in current namespace

kubectl get pods <pod_name>

displays information for single given pod

kubectl delete pod <pod_name>

kubectl apply -f <yaml_file_name>

kubectl create deployment <deployment_name> --image <image_path>

kubectl get pods -w

kubectl describe deployment <deployment_name>

kubectl get deployment <deployment_name> -o yaml

kubectl scale deployment <deployment_name> --replicas=2

kubectl edit deployment <deployment_name>

kubectl delete deployment <deployment_name>

kubectl set resources deployment hello-world --requests cpu=10m, memory=20Mi --limits cpu=80m, memory=100Mi

kubectl describe node node1

kubectl top nodes -l node -role.kubernetes.io/workes

kubectl create --save-config -f dev-quota.yml

kubectl create quota dev-quota --hard services=10, cpu=1300, memory 200Mi

kubectl get resourcequota

kubectl describe quota

kubectl delete resourcequota quota_name

Applying limit range

Kubectl create --save-config -f <filelename.yml>

kubectl describe limitrange limitrangeName

kubectl delete limitrange <name.

Probes to find app readiness, liveness and startup
