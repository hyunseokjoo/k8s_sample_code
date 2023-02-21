# pv pvc Sample Code

### pv pvc 실습 명령어

```bash
# pv pvc 생성
kubectl apply -f pv.yaml
kubectl apply -f pvc.yaml

# pv pvc 확인
kubectl get pv
kubectl get pvc

# pod 배포
kubectl apply -f pvc_pod.yaml

# pod들어가서 기존에 있던 file 확인
kubectl exec -it pvc-nfs-nginx -- /bin/bash
cd /usr/share/nginx/html
ls -al
```
