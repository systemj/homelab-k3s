# apps

## jellyfin
- https://github.com/jellyfin/jellyfin
- https://github.com/jellyfin/jellyfin-helm
```bash
kubectl -n kube-system create -f manifests/jellyfin/helmChart.yaml
```

## ollama
- https://docs.ollama.com/
- https://github.com/otwld/ollama-helm
```bash
kubectl -n kube-system create -f manifests/ollama/helmChart.yaml
```

## open-webui
- https://docs.openwebui.com/
- https://github.com/open-webui/helm-charts/tree/main/charts/open-webui
```bash
kubectl -n kube-system create -f manifests/open-webui/helmChart.yaml
```

## mcpo-time
- https://github.com/open-webui/mcpo
- https://github.com/modelcontextprotocol/servers/tree/main/src/time
```bash
kubectl -n kube-system create -f manifests/mcpo-time/helmChart.yaml
```

### add to open-webui
Admin Panel -> Settings -> External Tools -> +
- URL: http://mcpo-time.mcpo.svc.cluster.local:8000/time
- Visibility: Public
