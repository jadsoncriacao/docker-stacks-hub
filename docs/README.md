# Arquitetura e Serviços 🏛️

Este guia explica como a infraestrutura está organizada por categorias.

## 📂 Categorias

### 🏗️ Infraestrutura (`/infra`)
Serviços que mantêm o ecossistema funcionando.
- **[Traefik](./infra/traefik/traefik.md)**: Proxy reverso e gerenciamento de certificados.
- **[Portainer](./infra/portainer/portainer.md)**: Painel de controle visual para Docker.
- **[Docker](./infra/docker/docker.md)**: Comandos e boas práticas.

### 🐘 Bancos de Dados (`/database`)
Persistência de dados para outras stacks.
- **[PostgreSQL](./database/postgres/postgres.md)**: SQL Principal.
- **[pgAdmin](./database/pgadmin/pgadmin.md)**: Gestão web do Postgres.
- **[DbGate](./database/dbgate/dbgate.md)**: Gestão web multi-banco (GUI).
- **[SQL Server](./database/sqlserver/sqlserver.md)**: Microsoft SQL Server em container.

### 🔐 VPN & Segurança (`/vpn`)
Acesso remoto criptografado.
- **[Headscale](./vpn/headscale/headscale.md)**: Servidor de controle.
- **[Tailscale](./vpn/tailscale/tailscale.md)**: Cliente Gateway.

### 🚀 Aplicações
Stacks de uso final ou agrupadas.
- **[Nextcloud](./apps/nextcloud/nextcloud.md)**: Cloud pessoal.

### 🤖 IA
- **[Ollama](./ia/ollama/ollama.md)**: API local para rodar modelos.
- **[Open WebUI](./ia/open-webui/open-webui.md)**: UI web para conversar com modelos.

---
## 🚀 Como Inicializar

1. **Rede:** `docker network create local-network`
2. **Ordem recomendada:**
   ```bash
   docker compose -f dev/infra/traefik/docker-compose.yaml up -d
   docker compose -f dev/database/postgres/docker-compose.yaml up -d
   docker compose -f dev/infra/portainer/docker-compose.yaml up -d
   ```

---
[⬅ Voltar para o menu principal](../README.md)
