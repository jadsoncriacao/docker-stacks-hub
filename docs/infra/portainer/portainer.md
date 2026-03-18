# Documentação: Portainer 🚢

## 📋 O que é e para que serve?
O **Portainer** é uma interface de gerenciamento gráfica (GUI) para o Docker. Ele serve para facilitar a visualização e o controle de containers, imagens, redes e volumes sem a necessidade de usar apenas a linha de comando.

## ⚙️ Como funciona?
Ele se conecta ao socket do Docker (`/var/run/docker.sock`) para monitorar e comandar o ambiente. 
Neste projeto, ele permite o deploy via **GitOps**: você aponta o Portainer para este repositório Git, e ele baixa e sobe as stacks automaticamente.

## 🚀 Como usar / Acesso
- **URL Local**: [http://localhost:9000](http://localhost:9000)
- **Deploy via Git**: No menu `Stacks`, escolha `Add stack` > `Repository` e informe a URL deste repositório e o caminho do `docker-compose.yaml` desejado.

## 🛠️ Comandos Úteis
- **Logs do Portainer**: `docker logs portainer`
- **Reiniciar**: `docker compose restart` (dentro de `dev/infra/portainer`)

---
[⬅ Voltar para o menu principal](../../README.md)
