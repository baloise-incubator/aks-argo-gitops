# aks-argo-gitops

Create secrets in key vault first:
- cloudflare-api-key
- cloudflare-api-token

## Login with Azure CLI
Login to the cluster, see aks Overview -> Connect -> Azure CLI.

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
