# Documentação: Docker 🐳

## 📋 O que é e para que serve?
O **Docker** é uma plataforma de conteinerização que permite empacotar aplicações e suas dependências em ambientes isolados chamados containers. Ele garante que o software funcione da mesma forma, independentemente do ambiente onde está sendo executado.

Neste projeto, ele é a base de toda a infraestrutra, permitindo rodar bancos de dados, proxies e apps de forma modular.

## ⚙️ Como funciona?
- **Imagens**: Modelos de leitura que contêm tudo o que é necessário para rodar uma aplicação.
- **Containers**: Instâncias em execução dessas imagens.
- **Docker Compose**: Ferramenta usada para definir e rodar múltiplos containers de forma coordenada usando arquivos `.yaml`.

## 🚀 Como Inicializar o Projeto

1. **Criar Rede Externa**:
   ```bash
   docker network create local-network
   ```
2. **Ordem recomendada**:
   ```bash
   docker compose -f dev/infra/traefik/docker-compose.yaml up -d
   docker compose -f dev/database/postgres/docker-compose.yaml up -d
   docker compose -f dev/infra/portainer/docker-compose.yaml up -d
   ```

## 🛠️ Comandos Principais
- **Listar containers**: `docker ps`
- **Ver logs**: `docker logs <nome-do-container>`
- **Parar stack**: `docker compose down`

---
[⬅ Voltar para o menu principal](../../README.md)
