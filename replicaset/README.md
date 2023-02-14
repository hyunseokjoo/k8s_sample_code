# replicaset sample code
### 실습 명령어 순서
```bash
# create replicaset 
kubectl apply -f replicaset.yaml

# get replicaset info
kubectl get replicaset 
kubectl get rs 
kubectl get rs replica-sample -o wide

# get pod info
kubectl get pods --show-labels

# scaleup
kubectl apply -f replicaset_scaleup.yaml

# scale down
kubectl scale --replicas=2 replicaset replica-sample

# delete
kubectl delete replicaset replica-sample
```

### Replicaset관련 kubectl 명령어
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