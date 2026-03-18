# Documentação: Tailscale Gateway 🔗

## 📋 O que é e para que serve?
O **Tailscale** (neste contexto rodando como container) serve como um **Gateway de Rede**. Ele permite que dispositivos externos (como seu celular ou notebook fora de casa) acessem de forma segura os outros containers na rede `local-network` como se estivessem localmente.

## ⚙️ Como funciona?
Ele roda o cliente Tailscale dentro de um container que está conectado à rede Docker `local-network`.
- **Mesh VPN**: Ele cria um túnel criptografado seguro com o servidor Headscale.
- **Roteamento de Subrede**: Ele pode ser configurado para "anunciar" rotas, permitindo acesso a toda a rede interna do Docker pelo seu IP interno.
- **Exit Node**: Pode ser usado como um ponto de saída para navegar na internet usando o IP do servidor.

## 🚀 Como usar / Acesso
- **Autenticar o Container**:
  ```bash
  docker logs tailscale # Procure pelo link de autenticação
  ```
- **Login Manual**:
  ```bash
  docker exec -it tailscale tailscale up --login-server http://headscale:8080
  ```

---
[⬅ Voltar para o menu principal](../../README.md)
