# Laravel

## Erro de data 0000-00-00 vinda do banco

Rodar o seguinte commando dentro do prompt do MySql

```sql
SET GLOBAL sql_mode = 'NO_ZERO_DATE,NO_ZERO_IN_DATE';
```
