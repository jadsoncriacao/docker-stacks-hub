# Documentação: SQL Server 🧱

## 📋 O que é e para que serve?
O **Microsoft SQL Server** é um SGBD relacional. Nesta stack ele roda em container para desenvolvimento local e testes, expondo a porta padrão `1433`.

## ⚙️ Como funciona?
Dentro da rede Docker `local-network`, ele fica acessível pelo hostname `sqlserver`.
- **Persistência**: volume Docker `sqlserver_data` em `/var/opt/mssql`
- **Backups**: bind mount para `dev/database/sqlserver/backups` em `/var/opt/mssql/backup`
- **Porta**: `1433` (externa e interna)

## 🚀 Como subir
1) Crie um arquivo `.env` baseado no exemplo:
```bash
copy dev\\database\\sqlserver\\.env.example dev\\database\\sqlserver\\.env
```

2) Suba o serviço:
```bash
docker compose -f dev/database/sqlserver/docker-compose.yaml up -d
```

## 🔄 Restore de backup (`.bak`)
O stack monta `dev/database/sqlserver/backups` em `/var/opt/mssql/backup`. Então o `FROM DISK` deve apontar para esse caminho dentro do container.

> Ajuste os placeholders:
> - `NomeQueVoceQuiserDarAoBanco`
> - o arquivo `.bak` (ex.: `BKP-A24-20260301-2.bak`)
> - os nomes lógicos dos arquivos no `MOVE 'ITPPRODUCAO_Data'` e `MOVE 'ITPPRODUCAO_Log'` (esses nomes variam por backup; valide antes no seu `.bak`).

```sql
RESTORE DATABASE [NomeQueVoceQuiserDarAoBanco]
FROM DISK = '/var/opt/mssql/backup/BKP-A24-20260301-2.bak'
WITH
    RECOVERY,
    REPLACE,
    MOVE 'ITPPRODUCAO_Data' TO '/var/opt/mssql/data/NomeQueVoceQuiserDarAoBanco.mdf',
    MOVE 'ITPPRODUCAO_Log'  TO '/var/opt/mssql/data/NomeQueVoceQuiserDarAoBanco_log.ldf';
```

## 🔗 Conexão (exemplos)
- **Host (de fora do Docker)**: `localhost`
- **Host (dentro do Docker)**: `sqlserver`
- **Porta**: `1433`
- **Usuário**: `sa`
- **Senha**: valor de `MSSQL_SA_PASSWORD` no `.env`

---
[⬅ Voltar para o menu principal](../../README.md)

