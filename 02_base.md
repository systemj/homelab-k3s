# base services

## metallb
- https://metallb.io/installation/#installation-with-helm
- https://github.com/metallb/metallb
```bash
kubectl -n kube-system create -f manifests/metallb/helmChart.yaml
kubectl -n metallb-system create -f manifests/metallb/resources.yaml
```

## reflector
- https://github.com/emberstack/kubernetes-reflector
```bash
kubectl -n kube-system create -f manifests/reflector/helmChart.yaml
```

## cert-manager
- https://cert-manager.io/docs/installation/helm/
- https://github.com/cert-manager/cert-manager
```bash
kubectl -n kube-system create -f manifests/cert-manager/helmChart.yaml
kubectl -n cert-manager create -f manifests/cert-manager/resources.yaml
```

## tail-scale
- https://tailscale.com/kb/1236/kubernetes-operator
- https://github.com/tailscale/tailscale/releases
- https://github.com/tailscale/tailscale/tree/main/cmd/k8s-operator/deploy
```bash
kubectl -n kube-system create -f manifests/tailscale/helmChart.yaml
kubectl -n tailscale create -f manifests/tailscale/resources.yaml
```

### update ACLs
- https://login.tailscale.com/admin/acls/file
- tailscale/acl.json

