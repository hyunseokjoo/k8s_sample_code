# volume Sample Code

### volume 실습 명령어

```bash
# vm hostpath로 배포하기
kubectl apply -f ./hostPath.yaml

# pod로 들어가기
kubectl exec -it hostpath -- /bin/bash
# sample.txt file 생성
cd /var/share/nginx/html
touch sample.txt
ls -la

# vm nfs 배포하기
kubectl apply -f nfs.yaml

# Pod러 들어가기
kubectl exec -it nfs-nginx -- /bin/bash
# nfs mount 되었는지 확인
mount | grep nfs
# index.html file 생성
cd /usr/share/nginx/html
touch index.html
ls -al
exit

# 다른 pod 로 들어가 생성된 file 화깅ㄴ
kubectl exec -it nfs-nginx-check -- /bin/bash
cd  /usr/share/nginx/html
ls -la
```
