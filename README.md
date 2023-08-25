# aks-argo-gitops

Make sure that you are Cluster Admin.

## Login with Azure CLI
Login to the cluster, see Azure Portal -> Your AKS Cluster Overview -> Connect -> Azure CLI.

## Install external-dns including CRD's
```bash
kubectl apply -k external-dns
```

## Install ArgoCD including CRD's, point to this git repo
```bash
kubectl apply -k argocd
```

## Add Public IP of Ingress Controler to cloudflare
Set public ip address in cloudflare to ingress controller load balancer ip.
