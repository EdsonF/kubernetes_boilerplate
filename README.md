# Kubernetes Boilerplate

A kubernetes boilerplate to save precious minutes.

To get started:

```bash
kubectl apply -f admin-user.yml
```

Copy the output of the token from the next command if you wish to login to the dashboard

```bash
kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}')
```

```bash
kubectl proxy
```

Visit `http://localhost:8001/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/#!/login`