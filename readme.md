sysctl -a | grep -E --color 'machdep.cpu.features|VMX' 

curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl

chmod +x ./kubectl

sudo mv ./kubectl /usr/local/bin/kubectl

xcode-select --install (BEFORE MINIKUBE)

brew install minikube
