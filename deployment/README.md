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

# app history 확인 (--revision옵션은 특정 버전 선택)
kubectl rollout history deployment/deployment-sample
kubectl rollout history deployment/deployment-sample --revision=2

# app rollback
kubectl rollout undo deployment/deployment-sample --to-revision=1

# delete
kubectl delete deployment deployment-sample
```

### Deployment 관련 kubectl 명령어

```bash
# replicaset 생성
kubectl apply -f <replicaset yaml 파일 경로>

# replicaset 조회
kubectl get deployment
kubectl get deployment <replicasetName> -o wide
kubectl get all -o wide

# app history 확인
kubectl rollout history <deploymentName>/<deploymentAppName>

# app histroy 특정 옵션 선택
kubectl rollout history <deploymentName>/<deploymentAppName> --revision=<version>

# replicaset 삭제
kubectl delete deployment <deploymentName>
```
