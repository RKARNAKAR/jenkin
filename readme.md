# Jenkins Test Repo  
This is a simple test repo for Jenkins.   hii this is uday 
deploy a nginx service on minikube 
task : 

minikube service nginx --url

# 5) Open the URL in your default browser (example)
# run minikube service nginx --url, copy the printed URL (e.g. http://127.0.0.1:xxxxx) then:
Start-Process "http://127.0.0.1:xxxxx"

# OR from PowerShell programmatically:
$url = minikube service nginx --url
Start-Process $url

# 6) Scale the deployment to 4 replicas
kubectl scale deployment nginx --rep
