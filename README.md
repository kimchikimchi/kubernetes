# kubernetes-
Learn Kubernetes

# To run Minikube for local Kubernates session
# Installation
1. Install kubectl : brew install kubectl
2. Install minikube : brew cask install minikube
3. Install docker xhyve drive : brew install docker-machine-driver-xhyve

# To start/stop minikube 
minikube start --vm-driver=xhyve
minikube stop
minikube delete
minikube status

 
# Check what kubectl is hooked up to
kubectl config current-context

# List nodes in cluster
kubectl get nodes

# Create, apply changes, delete pods
kubectl create|apply|delete -f ./pod.yml 
 
# list pods
kubectl get pods


# Expose service layer  (when replication controller called 'hello-rc' is already created 
kubectl expose rc hello-rc --name=hello-svc --target-port=8080 --type=NodePort
kubectl delete svc hello-svc
