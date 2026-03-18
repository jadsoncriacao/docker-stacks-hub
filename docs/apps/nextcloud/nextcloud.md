# Documentação: Nextcloud ☁️

## 📋 O que é e para que serve?
O **Nextcloud** é uma plataforma de produtividade e armazenamento de arquivos em nuvem que você mesmo hospeda. Ele serve para substituir serviços como Google Drive ou Dropbox, permitindo que você tenha controle total sobre seus arquivos, fotos, contatos e calendários.

## ⚙️ Como funciona?
Ele é uma aplicação PHP que roda em cima de um servidor web. 
- **Persistência de Dados**: Seus arquivos reais ficam guardados em um volume Docker local.
- **Banco de Dados**: Ele usa o container do `postgres` para guardar metadados, configurações e informações de usuários.
- **Integração**: Ele se conecta ao banco via rede `local-network` usando as credenciais definidas no arquivo `.env`.

## 🚀 Como usar / Acesso
- **URL via Traefik (HTTPS)**: [https://nextcloud.localhost](https://nextcloud.localhost)
- **URL Direta (HTTP)**: [http://localhost:8081](http://localhost:8081)
- **Configuração de Domínios**: O sistema está configurado para aceitar qualquer domínio (`*`) via variável `NEXTCLOUD_TRUSTED_DOMAINS` para facilitar o acesso via IP na rede local.

> [!NOTE]
> Ao acessar via HTTPS, aceite o certificado auto-assinado no seu navegador pela primeira vez.

---
[⬅ Voltar para o menu principal](../../README.md)
