FROM ghcr.io/open-webui/mcpo:main

RUN uv tool install mcp-server-time

ADD config.json .

ENV PATH=PATH=/root/.local/bin:/app/.venv/bin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

EXPOSE 8000

ENTRYPOINT ["mcpo", "--config", "/app/config.json"]
