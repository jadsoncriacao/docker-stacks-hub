# Documentação: Headscale 🔐

## 📋 O que é e para que serve?
O **Headscale** é uma implementação de código aberto do servidor de controle do Tailscale. Ele serve para que você possa criar sua própria rede mesh VPN (Virtual Private Network) privada, sem depender da infraestrutura em nuvem da empresa Tailscale.

## ⚙️ Como funciona?
Ele atua como o "coordenador" da rede.
- **Coordenação**: Ele distribui as chaves de criptografia e as rotas entre os nós conectados.
- **Banco de Dados**: Utiliza o container do `postgres` para armazenar informações de usuários e dispositivos.
- **Protocolo**: Utiliza o protocolo WireGuard por baixo dos panos para conexões seguras e rápidas.

## 🚀 Como usar / Acesso
- **URL Dashboard**: [http://localhost:8082](http://localhost:8082) (se estiver usando uma interface visual opcional).
- **Criar Usuário**:
  ```bash
  docker exec -it headscale headscale users create meu-usuario
  ```
- **Listar Nós**:
  ```bash
  docker exec -it headscale headscale nodes list
  ```

---
[⬅ Voltar para o menu principal](../../README.md)
