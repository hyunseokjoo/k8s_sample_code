# service sample code

### service_nodeport 실습 명령어

```bash
# create service_nodeport
kubectl apply -f service_deployment.yaml

# get service_nodeport info
kubectl apply -f service_nodeport.yaml

# get service_nodeport info detail
kubectl get svc service-sample -o wide

# get node info detail
kubectl get nodes -o wide
```

nodeip:nodeport로 접속하여 확인

### service- LB 실습 명령어

```bash
# create LB service
kubectl apply -f service_loadbalancer.yaml

# get service info detail for getting external_ip
kubectl get svc -o wide
```

external_ip:port로 접속하여 확인

### ExternalName 실습 명령어

```bash
# create externalName service
kubectl apply -f externalName.yaml

# get pod id
kubectl get pod

# connect bash
kubectl exec -it {podID} -- /bin/bash
```

### ExternalName 실습 bash 명령어

```bash
# apt updates
apt-get updates

# install curl for testing
apt install curl

# request externalname-sample
curl externalname-sample
```

### External_ip 실습 명령어

```bash
# create deploy
kubectl apply -f externalIP_endpoint.yaml

# create service
kubectl apply -f externalIP_service.yaml

# get info svc
kubectl get svc

# get info enpoints
kubectl get endpoints

# connect bash
kubectl exec -it {podID} -- /bin/bash
```

### External_ip 실습 bash 명령어

```bash
# request externalip-svc
curl externalip-svc
```

### Headless_service 실습 명령어

```bash
# deployment(pods) 다시 배포
kubectl apply -f headless_deployment.yaml

# create headless_service
kubectl apply -f headless_service.yaml

# get pod info
kubectl get pod

# connect bash
kubectl exec -it {podID} -- /bin/bash
```

### Headless_service 실습 bash 명령어

```bash
# install dnsutils
apt install dnsutils

# check ip list in headless-svc
nslookup headless-svc

# check ip list in service-sample to compare with LB ip list
nslookup service-sample

# request headless-svc
curl headless-svc
```
