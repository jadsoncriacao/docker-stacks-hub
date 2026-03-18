# Documentação: pgAdmin 4 🛠️

## 📋 O que é e para que serve?
O **pgAdmin** é a ferramenta de administração e desenvolvimento para PostgreSQL mais popular. Ele serve para fornecer uma interface web amigável onde você pode criar tabelas, rodar queries SQL e gerenciar usuários do banco sem usar o terminal.

## ⚙️ Como funciona?
O pgAdmin roda como um servidor web independente que se conecta ao container do **PostgreSQL** através da rede interna. Ele permite gerenciar múltiplos servidores Postgres a partir de um único painel.

## 🚀 Como usar / Acesso
- **URL via Traefik (HTTPS)**: [https://pgadmin.localhost](https://pgadmin.localhost)
- **URL Direta (HTTP)**: [http://localhost:5050](http://localhost:5050)
- **Login**: `pgadmin@pgadmin.com`
- **Senha**: `pgadmin123`
- **Conectar ao Banco**: Ao adicionar um novo servidor, use o nome `postgres` no campo `Host name/address`, usuário `postgres` e senha `postgres123`.

---
[⬅ Voltar para o menu principal](../../README.md)
