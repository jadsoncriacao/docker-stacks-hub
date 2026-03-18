# Stacks de Produção 🚀

Este diretório é destinado a stacks que já estão rodando em produção.

## Padrões de Produção
- Use imagens com tags específicas (evite `:latest`).
- Configure políticas de reinicialização (`restart: always`).
- Gerencie segredos de forma segura (Docker Secrets ou arquivos de ambiente restritos).
- Mantenha backups dos volumes persistentes.

---
[⬅ Voltar para o menu principal](../README.md)
