# mcpo-time

## build
```bash
docker build -t systemj/mcpo-time .
helm package chart
```

## publish
```bash
docker push systemj/mcpo-time
helm push mcpo-time-0.1.0.tgz oci://registry-1.docker.io/systemj
```

## upstream:
- https://github.com/open-webui/mcpo
- https://github.com/modelcontextprotocol/servers/tree/main/src/time

## add to open-webui
Admin Panel -> Settings -> External Tools -> +
- URL: http://mcpo-time.mcpo.svc.cluster.local:8000/time
- Visibility: Public
