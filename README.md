# GMC_k8s
K8s YAML Configuration File

# Steps to deploy https://github.com/khouloudRb/K8s_repo.git to K8s cluster (using minikube)

* start minikube and install ingress controller 
* *minikube start 
minikube addons enable ingress
Apply K8s Manifest files 
kubectl apply -f mongo-secret.yaml 
kubectl apply -f backend.yaml
kubectl apply -f frontend-ingress.yaml
kubectl apply -f frontend.yaml
add ip address of the host to /etc/hosts
kubectl get ingress > get the generated  ip address
