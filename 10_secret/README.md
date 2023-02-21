# secret Sample Code

### secret 실습 명령어

```bash
# secrets/db.password 내용 secret 객체로 만들기
kubectl create secret generic db-config --from-file=secrets/db.password       
or
kubectl create secret generic db-config --from-file=secrets/ 

# yaml 파일로 db-config 내용 출력
kubectl get secret db-config -o yaml 

# container 안에 파일 읽기
kubectl exec -it secret-sample -- /bin/bash
cd var/share/nginx/html
ls -al
cat db.password
```
