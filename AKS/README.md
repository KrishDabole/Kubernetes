docker images
docker tag empform:0.1 acrtest.azurecr.io/empform:0.1
docker login acrtest.azurecr.io
docker push acrtest.azurecr.io/empform:0.1

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