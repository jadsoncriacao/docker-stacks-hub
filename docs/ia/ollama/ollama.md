# Documentação: Ollama 🧠

## 📋 O que é e para que serve?
O **Ollama** é um framework que permite rodar modelos de linguagem de grande escala (LLMs), como Llama 3 ou Mistral, diretamente no seu próprio hardware. Ele serve para prover uma API local de IA sem depender de serviços em nuvem ou conexões externas.

## ⚙️ Como funciona?
Ele gerencia o carregamento dos modelos na CPU ou GPU e expõe uma API REST.
- **Armazenamento**: Os modelos baixados são armazenados no volume `ollama_data`.
- **API**: Por padrão, o Ollama atende na porta `11434`. Outros serviços (como o Open WebUI) se conectam a ele através dessa porta na rede Docker.

## 🚀 Como usar / Acesso
- **Baixar um modelo**: 
  ```bash
  docker exec -it ollama ollama pull llama3
  ```
- **Interagir via CLI**:
  ```bash
  docker exec -it ollama ollama run llama3
  ```

---
[⬅ Voltar para o menu principal](../../README.md)
