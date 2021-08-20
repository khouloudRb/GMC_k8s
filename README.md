# GMC_k8s
K8s YAML Configuration File

Steps to deploy https://github.com/khouloudRb/K8s_repo.git to K8s cluster (using minikube)

* Start minikube and install ingress controller 
  * minikube start 
  * minikube addons enable ingress
* Apply K8s Manifest files 
  * kubectl apply -f mongo-secret.yaml 
  * kubectl apply -f backend.yaml
  * kubectl apply -f frontend-ingress.yaml
  * kubectl apply -f frontend.yaml
* Add ip address of the host to /etc/hosts
  * kubectl get ingress > get the generated  ip address
  * sudo vim /etc/hosts and add the ip address as well as the host name specified in frontend-ingress.yaml
