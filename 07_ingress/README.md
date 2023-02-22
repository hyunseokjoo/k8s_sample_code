# Ingress IngressController Sample Code

### Ingress IngressController 실습 명령어

```bash
# deployment, service 배포
kubectl apply -f serviceAccount.yaml
kubectl apply -f serviceMenu.yaml   
kubectl apply -f serviceSales.yaml 

# deployment, service 배포 확인
kubectl get deploy
kubectl get svc

# nginx-ingress Controller 다운 및 배포 
kubectl create clusterrolebinding cluster-admin-binding \
  --clusterrole cluster-admin \
  --user $(gcloud config get-value account)

kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.6.4/deploy/static/provider/cloud/deploy.yaml

# ingress-nginx namespace 확인 
kubectl get namespace  

# ingress-nginx pod, service LB 확인
kubectl get all -n ingress-nginx

# backend 정보가 있는 ingress 배포
kubectl apply -f ingress.yaml
```
