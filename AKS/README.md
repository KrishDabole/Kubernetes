sudo apt update && apt upgrade -y

sudo apt-get install docker.io -y
docker build -t empform:0.1 .

docker images
docker tag empform:0.1 acrtest.azurecr.io/empform:0.1
docker login acrtest.azurecr.io
docker push acrtest.azurecr.io/empform:0.1

curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
az login --tenant "00fa9ac5-cc69-48b1-bab5-618b4e4c8aaf"

kubectl get ns
kubectl get nodes
kubectl get nodes -o wide
kubectl get pods
kubectl get pods -A
kubectl get pods -o wide
kubectl apply -f dep.yaml
kubectl get svc
kubectl describe pod <podname>
kubectl logs <podname>
kubectl exec -ti <podname> -- /bin/bash