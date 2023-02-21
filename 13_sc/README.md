# StorageClass Sample Code

### StorageClass 실습 명령어

```bash
# ServiceAccount 생성
kubectl apply -f serviceAccount.yaml

# nfs-ganesha-server-and-external-provisioner 배포
kubectl apply -f provisioner.yaml

# storageClass 배포
kubectl apply -f storageClass.yaml

# storageClass를 이용한 pvc 배포
kubectl apply -f storageClass_pvc.yaml

# pvc를 이용한 pod 배포
kubectl apply -f storageClass_pod.yaml

# 파일 생성
kubectl exec -it pvc-nfs-nginx -- /bin/bash
cd  /usr/share/nginx/html
touch sample.txt

# 파일 공유 되었는지 확인
kubectl exec -it pvc-nfs-nginx-check -- /bin/bash
cd  /usr/share/nginx/html
ls -al
```
