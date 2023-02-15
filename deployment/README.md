# Deployment sample code

### Deployment 실습 명령어

```bash
# create deployment
kubectl apply -f deployment_v1.yaml

# deployment 확인
kubectl get deployment

# deployment의 replicaset 확인하기
kubectl get replicaset

# deployment의 pod 확인하기
kubectl get pod

# pod 확인
kubectl get pod -o wide

# pod 장애 실행
kubectl delete pod {pod중 하나 기입}
kubectl get pod -o wide

# deployment update
kubectl apply -f deployment_v2.yaml

# scale down


# delete
kubectl delete replicaset replica-sample
```

### Deployment 관련 kubectl 명령어

```bash
# replicaset 생성
kubectl apply -f <replicaset yaml 파일 경로>

# replicaset 조회
kubectl get rs
kubectl get rs <replicasetName> -o wide
kubectl get pods --show-labels

# replicaset scaling
kubectl scale --replica=<Num> replicaset <replicasetName>

# replicaset 삭제
kubectl delete replicaset <replicasetName>
```
