# Documentação: PostgreSQL 🐘

## 📋 O que é e para que serve?
O **PostgreSQL** é um sistema de gerenciamento de banco de dados relacional (SGBD) extremamente robusto e de código aberto. Ele serve para armazenar de forma segura e estruturada os dados de nossas aplicações (como o Nextcloud e o Headscale).

## ⚙️ Como funciona?
Ele funciona como um servidor central de dados. Dentro da rede Docker `local-network`, ele é acessível pelo nome de host `postgres`. 
- **Persistência**: Os dados são salvos em volumes Docker para não serem perdidos quando o container é reiniciado.
- **Porta**: A porta padrão interna é `5432`.

## 🚀 Como usar / Acesso
- **Host**: `postgres`
- **Usuário padrão**: `postgres` (definido no `.env`)
- **Senha padrão**: `postgres123`
- **Acesso via Terminal**:
  ```bash
  docker exec -it postgres psql -U postgres -d postgres
  ```

---
[⬅ Voltar para o menu principal](../../README.md)
