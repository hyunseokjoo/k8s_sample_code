# k8s_sample_code

### Pod 관련 Sample 명령어

```bash
# check pod info
kubectl apply -f pod.yaml

# check pod detail info
kubectl get pod -o wide

# execute
kubectl exec nginx -c nginx -- echo 1

# check pod env
kubectl exec nginx -c nginx -- env

# port-forwarding
kubectl port-forward nginx 8080:80

# delete pod
kubectl delete pod nginx
```

### Pod 관련 명령어 정리

```bash
# pod 생성
kubectl apply -f <yaml파일 경로>
kubectl apply -f pod.yaml

# 모든 pod 확인
kubectl get pods

# pod 실행 및 ip 확인
kubectl get pod -o wide

# pod 종료
kubectl delete pod --all
kubectl delete pod <pod-name>

# 컨테이너 IP확인
kubectl exec <pod-name> [-c <container-name>] --ifconfig eth0

# 컨테이너 환경 변수 확인
kubectl exec <pod-name> --env

# 포트 포워딩
kubectl port-forward <pod-name> <host-port>:<container-port>
```
