
Instalar todas as versões que deseja usar no sistema:

```bash
sudo apt install php8.3 php8.4
```


Configurar as alternativas possíveis:

```bash
sudo update-alternatives --install /usr/bin/php php /usr/bin/php8.3 1
sudo update-alternatives --install /usr/bin/php php /usr/bin/php8.4 2
```


Para selecionar a versão que deseja rodar:

```bash
sudo update-alternatives --config php
```

O resultado deve ser algo similar ao abaixo:

![[Pasted image 20241109105403.png]]