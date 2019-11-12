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
