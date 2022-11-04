[Installation Argo CD](https://argo-cd.readthedocs.io/en/stable/cli_installation/)

For working in UI:
```
kubectl get service -n argocd
```

Find argocd-server and do port-forward:
```
kubectl port-forward svc/argocd-server -n argocd 8080:443
```
In your localhost:8080 login is **admin** and your password you can check:
```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
```
