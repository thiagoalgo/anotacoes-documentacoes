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

## Modo DEBUG

Para habilitar o modo debug do Wordpress, para usar em ambiente de desenvolvimento, basta adicionar a linha abaixo ao arquivo wp-config.php
```php
define('WP_DEBUG', true);
```


## Anatomia de um tema WordPress

![[WordPress-Theme-Anatomy (1).png]]

## Passos para a criação de um tema

1. Criar a pasta do tema em wp-content/themes
2. Criar os arquivos index.php e style.php
3. Colocar os dados sobre o tema no arquivo style.php
4. Adicionar um screenshot do tema em formato png com 1200x900
5. Ativar o tema no painel do administrativo







## Links úteis


| Tema                    | Link                                                                                 |
| ----------------------- | ------------------------------------------------------------------------------------ |
| Referência da Funções   | https://developer.wordpress.org/reference/                                           |
| Padrões de documentação | https://developer.wordpress.org/coding-standards/inline-documentation-standards/php/ |
| Meta tags               | https://codex.wordpress.org/Meta_Tags_in_WordPress                                   |
|                         |                                                                                      |
