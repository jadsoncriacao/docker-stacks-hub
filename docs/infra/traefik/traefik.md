# Documentação: Traefik 🚦

## 📋 O que é e para que serve?
O **Traefik** é um roteador de borda (Edge Router) e Proxy Reverso moderno. Ele serve para receber todas as requisições web que chegam ao servidor e direcioná-las para o container correto, além de lidar automaticamente com certificados SSL e balanceamento de carga.

## ⚙️ Como funciona?
Ele monitora o socket do Docker em tempo real. Quando um novo container sobe com "labels" específicas do Traefik, ele cria automaticamente uma rota sem precisar reiniciar.
- **Roteamento**: Usa regras baseadas em Host ou Path.
- **Dashboard**: Oferece uma visão em tempo real de todas as rotas e serviços ativos.

## 🚀 Como usar / Acesso
- **Dashboard Visual**: [http://localhost:8080](http://localhost:8080)
- **Entrypoints**:
  - `web` (Porta 80): Redireciona automaticamente para HTTPS.
  - `websecure` (Porta 443): Tráfego criptografado com SSL auto-assinado.

## 🔗 Links Úteis
- [Documentação Oficial](https://doc.traefik.io/traefik/)

---
[⬅ Voltar para o menu principal](../../README.md)
