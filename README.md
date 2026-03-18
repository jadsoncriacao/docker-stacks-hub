# 🐳 Docker Stacks Hub

Repositório centralizado e profissional para o gerenciamento de infraestrutura Docker, organizado por categorias.

---

## 🏗️ Estrutura do Projeto

O projeto é dividido em categorias lógicas para facilitar a manutenção e escalabilidade:

*   📂 **`dev/infra/`**: Serviços base de infraestrutura (Traefik, Portainer).
*   📂 **`dev/database/`**: Bancos de dados e ferramentas de gestão SQL.
*   📂 **`dev/vpn/`**: Soluções de acesso remoto seguro (Headscale, Tailscale).
*   📂 **`dev/apps/`**: Aplicações (ex.: Nextcloud).
*   📂 **`dev/ia/`**: Serviços de Inteligência Artificial (ex.: Ollama + Open WebUI).
*   📂 **`docs/`**: Documentação modular seguindo a mesma estrutura de pastas.

---

## 📚 Documentação e Guias

Acesse os guias detalhados em [**docs/README.md**](./docs/README.md) ou pelos links abaixo:

| Categoria | Serviços |
| :--- | :--- |
| **Infra & Docker** | [🐳 Docker](./docs/infra/docker/docker.md) • [🚢 Portainer](./docs/infra/portainer/portainer.md) • [🚦 Traefik](./docs/infra/traefik/traefik.md) |
| **Bancos de Dados** | [🐘 PostgreSQL](./docs/database/postgres/postgres.md) • [🛠️ pgAdmin](./docs/database/pgadmin/pgadmin.md) • [🧰 DbGate](./docs/database/dbgate/dbgate.md) • [🧱 SQL Server](./docs/database/sqlserver/sqlserver.md) |
| **VPN & Acesso** | [🔐 Headscale](./docs/vpn/headscale/headscale.md) • [🔗 Tailscale](./docs/vpn/tailscale/tailscale.md) |
| **Aplicações** | [☁️ Nextcloud](./docs/apps/nextcloud/nextcloud.md) |
| **IA** | [🧠 Ollama](./docs/ia/ollama/ollama.md) • [🧠 Open WebUI](./docs/ia/open-webui/open-webui.md) |

---

## 🔗 Acesso via Traefik (DNS Local)

Com o Traefik ativo, você pode acessar os serviços pelos domínios `.localhost`. Isso elimina a necessidade de decorar portas.

| Serviço | URL de Acesso (HTTPS) | Link Direto (HTTP) |
| :--- | :--- | :--- |
| **Dashboard Traefik** | [http://localhost:8080](http://localhost:8080) | - |
| **Portainer** | [https://localhost:9443](https://localhost:9443) | [http://localhost:9000](http://localhost:9000) |
| **Nextcloud** | [https://nextcloud.localhost](https://nextcloud.localhost) | [http://localhost:8081](http://localhost:8081) |
| **pgAdmin** | [https://pgadmin.localhost](https://pgadmin.localhost) | [http://localhost:5050](http://localhost:5050) |
| **DbGate** | [https://dbgate.localhost](https://dbgate.localhost) | [http://localhost:3000](http://localhost:3000) |
| **Open WebUI (AI)** | [https://ai.localhost](https://ai.localhost) | [http://localhost:3000](http://localhost:3000) |

> [!IMPORTANT]
> **SSL Local**: O sistema utiliza certificados auto-assinados. Ao acessar via HTTPS, seu navegador exibirá um alerta de segurança. Clique em **"Avançado"** e **"Prosseguir"** para garantir a conexão criptografada.

---

## 🚀 Guia de Inicialização Rápida

1.  **Criar Rede Externa:**
    ```bash
    docker network create local-network
    ```

2.  **Subir Infraestrutura Base:**
    ```bash
    docker compose -f dev/infra/traefik/docker-compose.yaml up -d
    docker compose -f dev/database/postgres/docker-compose.yaml up -d
    docker compose -f dev/infra/portainer/docker-compose.yaml up -d
    ```

---
> *Este repositório é focado em modularidade e padrões GitOps.* 🚀