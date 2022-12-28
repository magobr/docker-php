# Docker PHP (7.4)
Esse é um repositório dedicado a facilitar a execução de projetos PHP (7.4)

### Esse container
O container está configurado para executar o php a nível de desenvolvimento, contendo:
- PHP (7.4.3)
- MySql (5.7)
- xdebug (3.1.5)
- Nginx (latest)
- composer (latest)

### Estrutura
- \docker
    - Dockerfile
    - \nginx
        - defaut.conf
        - host.cert
        - nopassword.key
- \src
    - index.php

A pasta **src** é onde os arquivos do projeto php devem estar.

### Como executar
1. Para executar é nescessário que tenha o **Docker** e **Docker compose** instalados
2. Com os requisitos ja prontos, para colocar os containers em execução execute o seguinte comando para construir os containers:
```
docker compose build 
```
3. Logo em seguida, executa o seguinte comandao para inicializar os container construidos:
```
docker compose up 
```

### Utilizando o Composer
O composer está instalado internamente pois depende do PHP para sua execução.
1. Primeiro, execute esse comando para entrar no bash do container PHP
```
docker exec -it php-docker bash
```
2. Estrando dentro do terminal, poderá usar os comandos **composer** para gestão de dependencias. Ex:
```
composer install
```