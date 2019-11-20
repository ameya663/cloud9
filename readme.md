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
      
      
   brew install docker-credential-helper-ecr
IN>> ~/.docker/config.json

{
	"credHelpers": {
		"aws_account_id.dkr.ecr.region.amazonaws.com": "ecr-login"
	}
}

IN>> nano ~/.aws/credentials


minikube service drt-darp-solver-frontend -n drt --url

kubectl get pods -n drt
kubectl logs [POD_NAME] -n drt

kubectl exec osrm-routing-core-cd86cd8dd-v7bm4 -n drt -i -t -- /bin/sh

Grafana port forwarding
kubectl --namespace monitoring port-forward grafana-59999fcf64-vzlrs 3000
