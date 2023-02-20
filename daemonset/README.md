# Daemonset sample code

### Daemonset 실습 명령어

```bash
# deploy daemonset
kubectl apply -f daemonset_without_nodeSelector.yaml

# check daemonset
kubectl get ds

# check pod
kubectl get pod

# check node id
kubectl get nodes

# set node label
kubectl label nodes <nodeName> <key>=<value>

# check node label
kubectl describe node <nodeName>

# deploy daemonset with nodeSelector
kubectl apply -f daemonset_with_nodeSelector.yaml

# check pod with node
kubectl get pod -o wide
```
