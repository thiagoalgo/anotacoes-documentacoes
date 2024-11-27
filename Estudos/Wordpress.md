## Dados de acesso no ambiente de desenvolvimento

Banco de dados:
- Host: localhost
- User: wordpress
- Pass: password

Admin Wordpress
- User: admin
- Pass: password

## Urls amigáveis (ambiente local)

Para URLs amigáveis em ambiente local com o servidor built-in do php é preciso criar um arquivo de rota (route.php) e iniciar o servidor php apontando para esse arquivo:

```php
<?php
// route.php
// Roteador para redirecionar todas as requisições ao index.php
if (php_sapi_name() == 'cli-server') {
    $_SERVER['SCRIPT_NAME'] = '/index.php';
}
return false;
?>
```

```bash
php -S localhost:8000 -t . router.php
```

Também é preciso configurar o formato das urls amigáveis no admin:

![[Pasted image 20241127175502.png]]