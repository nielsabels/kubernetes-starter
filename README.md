installing the dashboard

```
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.6.1/aio/deploy/recommended.yaml
```

making the dashboard accessible
```
kubectl apply -f dashboard-clusterrolebinding.yaml
kubectl apply -f dashboard-adminuser.yaml
kubectl -n kubernetes-dashboard create token admin-user
```

starting the dashboard
```
kubectl proxy
```

use nginx-deployment.yaml for a sample deployment