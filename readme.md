# Jenkins Test Repo  
This is a simple test repo for Jenkins.   hii this is uday 
deploy a nginx service on minikube 
task : 
start minkube 
deploy nginx 
expose and access service 
scale the deployment to 4 and show thr running pods 
expecetd output :
commands used 
screesnshot of nginx service 
# 1) Start minikube (use your driver, e.g. docker)
minikube start --driver=docker

# 2) Create nginx deployment
kubectl create deployment nginx --image=nginx

# 3) Expose deployment as a service (NodePort)
kubectl expose deployment nginx --type=NodePort --port=80

# 4) Show service and get the access URL
kubectl get svc nginx
minikube service nginx --url

# 5) Open the URL in your default browser (example)
# run minikube service nginx --url, copy the printed URL (e.g. http://127.0.0.1:xxxxx) then:
Start-Process "http://127.0.0.1:xxxxx"

# OR from PowerShell programmatically:
$url = minikube service nginx --url
Start-Process $url

# 6) Scale the deployment to 4 replicas
kubectl scale deployment nginx --rep
