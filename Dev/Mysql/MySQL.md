# Mysql & MariaDB

&nbsp;
## Exportar (dump) e Importar banco de dados

### Servidor Remoto
Gerar dump do banco de dados:

```bash
mysqldump -urhnb -p rhnb_bar > /home/ubuntu/.rhnb_backups/backup-bar_rhnb-dev.sql
```

### Servidor Local 

Buscar arquivo gerado no servidor remoto:

```bash
scp -i ~/.ssh/rhnb.pem ubuntu@rhnb.com.br:/home/ubuntu/.rhnb_backups backup-bar_rhnb-dev.sql  /home/thiago/backup-bar_rhnb-dev.sql
```

Importar:

```bash
mysql -uroot -p --database="rhnb_bar" < "/home/thiago/backup-bar_rhnb-dev.sql"
```

## Erro de data 0000-00-00 vinda do banco

Rodar o seguinte commando dentro do prompt do MySql

```sql
SET GLOBAL sql_mode = 'NO_ZERO_DATE,NO_ZERO_IN_DATE';
```
