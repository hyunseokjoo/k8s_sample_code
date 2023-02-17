# Deployment Strategy Sample Code

### Deployment Strategy - Recreate

```bash
# Create Initial deployment
kubectl apply -f start.yaml

# Deployment Recreate
kubectl apply -f strategy_recreate.yaml

# Check Pod Status
kubectl get pod -o wide
```

### Deployment Strategy - Rolling

```bash
# Create Initial deployment
kubectl apply -f start.yaml

# Deployment Recreate
kubectl apply -f strategy_rolling.yaml

# Check Pod Status
kubectl get rs
```