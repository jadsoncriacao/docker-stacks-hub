# Documentação: Open WebUI 🧠

## 📋 O que é e para que serve?
O **Open WebUI** (antigo Ollama WebUI) é uma interface de usuário rica e extensível para interagir com modelos de linguagem (LLMs). Ele serve como um "ChatGPT" local que se conecta ao seu servidor Ollama.

## ⚙️ Como funciona?
Ele é uma aplicação web que atua como frontend para a API do Ollama.
- **Integração**: Conecta-se ao container `ollama` via rede interna `local-network`.
- **Modelos**: Permite baixar, gerenciar e conversar com modelos (Llama, Gemma, Mistral, etc).
- **Persistência**: Mantém seu histórico de conversas e documentos em um volume Docker.

## 🚀 Como usar / Acesso
- **URL via Traefik (HTTPS)**: [https://ai.localhost](https://ai.localhost)
- **URL Direta (HTTP)**: [http://localhost:3000](http://localhost:3000)

> [!IMPORTANT]
> **Primeiro acesso**: Pode demorar alguns minutos na primeira vez enquanto o sistema baixa arquivos essenciais do HuggingFace e prepara o banco de dados.

## 🔐 Credenciais Padrão
- **E-mail**: `open-webui@open-webui.com`
- **Senha**: `open-webui123`

---
[⬅ Voltar para o menu principal](../../README.md)
