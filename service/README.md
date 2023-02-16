# ReplicaSet sample code

### ReplicaSet 실습 명령어

```bash
# create replicaset
kubectl apply -f replicaset.yaml

# get replicaset info
kubectl get replicaset
kubectl get rs
kubectl get rs replica-sample -o wide

# get replicaset info detail
kubectl describe rs replica-sample

# get pod info
kubectl get pods --show-labels

# get events info 시간별 정렬
kubectl get events --sort-by=metadata.creationTimestamp

# scaleup
kubectl apply -f replicaset_scaleup.yaml

# scale down
kubectl scale --replicas=2 replicaset replica-sample

# delete
kubectl delete replicaset replica-sample
```

### ReplicaSet관련 kubectl 명령어

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
