sysctl -a | grep -E --color 'machdep.cpu.features|VMX' 

brew install kubectl
brew link kubernetes-cli

brew link --overwrite kubernetes-cli

xcode-select --install (BEFORE MINIKUBE)

brew install minikube


DASHBOARD:

sudo kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0-beta4/aio/deploy/recommended.yaml

kubectl proxy

http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/


minikube dashboard


CONTAINER REGISTRY:
minikube start
minikube addons enable ingress
minikube addons configure registry-creds
minikube addons enable registry-creds
kubectl apply -f deployment.yaml


spec:
  template:
    spec:
      containers:
      - name: my-container
        image: ACCOUNT_ID.dkr.ecr.us-east-1.amazonaws.com/ECR_REPO:latest
      imagePullSecrets:
      - name: awsecr-cred
