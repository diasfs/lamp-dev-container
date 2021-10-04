# VSCode DevContainer Lamp, PHPMyAdmin e nodejs #

## Requisitos ##

- Docker
- Docker Compose
- Extensão Remote Development para VSCode

## Opcionais ##

- mkcert (https em localhost)
- Extensão xdebug para VSCode

## Arquivos de Configuração ##

Os seguintes arquivos serão copiados para dentro do container:

- php/etc/apache2/apache2.conf
- php/etc/apache2/sites-enabled/*
- php/etc/ssl/certs/*
- php/usr/local/etc/php/conf.d/*

## Personalização ##

- É possível personalizar o container principal através do arquivo php/Dockerfile
- É possível personalizar o conjuto de containers no arquivo docker-compose.yml:
    - dados de conexão ao mysql
    - portas expostas
    - volumes montados
    - variáveis de ambiente
    - etc

## Extensões do PHP pré-instaladas ##

- gd 
- imagick 
- xdebug 
- composer 
- opcache 
- soap 
- pdo 
- pdo_mysql

## Módulos do Apache pré-habilitadas ##

- rewrite
- ssl