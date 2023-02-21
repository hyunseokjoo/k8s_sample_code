# Taint_Tolerations Sample Code

### Taint_Tolerations 실습 명령어

```bash
# check node
kubectl get node

# set taint at a node
kubectl taint nodes <nodeName> <key>=<value>:<option>
kubectl taint nodes gke-my-cluster-default-pool-c66689e3-a3s3 gpu=false:NoSchedule

# check setting taint in the node
kubectl describe node <nodeName>
kubectl describe node gke-my-cluster-default-pool-c66689e3-a3s3

# deploy daemonset without toleration
kubectl apply -f <yaml file path>
kubectl apply -f ./daemonset_without_tol.yaml

# check pod
kubectl get pod -o wide

# deploy daemonset with toleration
kubectl apply -f ./daemonset_with_tol.yaml

# check pod
kubectl get pod -o wide

# delete taint
kubectl taint nodes <nodeName> <key>=<value>:<option>-
kubectl taint nodes gke-my-cluster-default-pool-c66689e3-a3s3 gpu=false:NoSchedule-
```

### Toleration 옵션

위에 작성한 toleration 자세한 옵션은 [이 곳](https://kubernetes.io/docs/concepts/scheduling-eviction/taint-and-toleration/)을 보고 작성

- key - taint에서 설정한 key값
- value - key에 해당하는 value
- operator - 조건절 삽입 가능
  - Equal - key value 동일 해야지 taint pod 생성 가능
  - Exists - key값이 존재 하는지 여부에 따라 pod 생성 가능
- effect - 오염지역 배포 규칙 정의
  - NoSchedule - 스케쥴러에서 스케쥴링 하지 말라고 명령, 실행 중이던 pod는 계속 실행됨
  - NoExecute - 실행 금지, pod가 존재한다면 삭제됨
  - PreferNoSchedule - 배치를 하지 않지만 다른데 갈 데 없으면 불가피하게 함
