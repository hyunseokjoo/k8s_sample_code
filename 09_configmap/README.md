# configmap Sample Code

### configmap 실습 명령어

```bash
# configs 내용 configmap 객체로 만들기
kubectl create configmap sample-config --from-file=configs

# yaml 파일로 sample-config 내용 출력
kubectl get configmap sample-config -o yaml 

# env ref 버전 pod 배포 
kubectl apply -f ./configmap_ref.yaml

# env 확인
kubectl exec -it config-ref-sep-sample -- env
kubectl exec -it config-ref-sample -- env     

# configmap volume 버전 pod 배포 
kubectl apply -f ./configmap.yaml

# container 안에 파일 읽기
kubectl exec -it configmap-sample -- /bin/bash
cd var/share/nginx/html
ls -al
cat STUDENT_NAME
cat SUBJECT
```
