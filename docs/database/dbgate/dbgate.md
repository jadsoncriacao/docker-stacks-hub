# Documentação: DbGate 🧰

## 📋 O que é e para que serve?
O **DbGate** é uma interface web para administração de bancos de dados (multi-banco). Ele serve como alternativa leve a ferramentas como pgAdmin/DBeaver, facilitando conexões e consultas em ambientes Docker.

## ⚙️ Como funciona?
O serviço roda dentro da rede Docker `local-network` e pode ser acessado:
- **Via Traefik (recomendado)**: `https://dbgate.localhost`
- **Via porta local**: `http://localhost:3000`

> Dentro da rede Docker, ele conversa com os bancos pelos nomes de serviço (ex.: `postgres`, `sqlserver`).

## 🚀 Como subir
```bash
docker compose -f dev/database/dbgate/docker-compose.yaml up -d
```

## 🔗 Acesso
- **URL (HTTPS / Traefik)**: `https://dbgate.localhost`
- **URL (HTTP / Porta)**: `http://localhost:3000`

---
[⬅ Voltar para o menu principal](../../README.md)

