
docker version

minikube config set driver docker

minikube delete --all --purge    # remove old cluster & profile
minikube config unset driver     # stop forcing docker driver

Get-VMSwitch

minikube start --driver=hyperv --hyperv-virtual-switch "Default Switch"

minikube delete --all --purge
minikube config set driver docker
minikube start --driver=docker
minikube status
minikube version

 kubectl create deployment mynginx --image=nginx
kubectl get deployment
kubectl set image deployment/mynginx nginx=nginx:latest
 kubectl get pods
 kubectl describe pods
kubectl expose deployment mynginx --type=NodePort --port=80 --target-port=80
 kubectl scale deployment mynginx --replicas=4
kubectl get service mynginx
kubectl port-forward svc/mynginx 8081:80
minikube tunnel
minikube delete
docker pull jasonrivers/nagios:latest
docker run --name nagiosdemo -p 8888:80 jasonrivers/nagios:latest
docker stop nagiosdemo
docker rm nagiosdemo
 docker images
docker rmi jasonrivers/nagios:latest
