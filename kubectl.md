# kubectl cheat sheet
```bash
kubectl get po
kubectl run --generator=run-pod/v1 nginx --image=nginx
kubectl describe po newpods-9kssz | grep -i image
kubectl delete po webapp
kubectl run --generator=run-pod/v1 redis --image=redis123 --dry-run -o yaml > redis-pod.yaml
kubectl create -f redis-pod.yaml
kubectl edit po redis

kubectl get rs
kubectl delete rs replicaset-1
kubectl delete po -lname=busybox-pod
kubectl scale rs new-replica-set --replicas=5

kubectl get deploy
kubectl get deploy frontend-deployment -o yaml
kubectl create deployment my-dep --image=busybox
kubectl create deploy httpd-frontend --image=httpd:2.4-alpine --dry-run -o yaml > httpd-deploy.yaml

kubectl get ns
kubectl -n research get po
kubectl -n finance run --generator=run-pod/v1 redis --image=redis
kubectl get po --all-namespaces

kubectl get svc
kubectl scale deploy webapp --replicas=3
```
