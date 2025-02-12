# Configuração Automatizada do Docker para Laravel

Este repositório fornece uma solução rápida e eficiente para configurar um ambiente de desenvolvimento Laravel usando Docker. O objetivo é automatizar todo o processo de criação e configuração de contêineres, permitindo que você comece seu projeto Laravel sem se preocupar com a configuração manual do ambiente.

## Funcionalidades

- Configuração automatizada do Docker para PHP, Nginx, MySQL e Redis.
- Certificados SSL autoassinados para desenvolvimento local.
- Configuração de fila com `php artisan queue:work`.
- Fácil de personalizar e adaptar para outros projetos Laravel.

## Pré-requisitos

Antes de começar, certifique-se de ter o seguinte instalado:

- Docker
- Docker Compose

## Começando

Para começar com este projeto, siga estas etapas:

1. Clone este repositório:

   ```bash
   git clone https://github.com/mavazca/laravel-docker-setup
   cd laravel-docker-setup
   ```

2. Copie o arquivo .env.example para .env

   ```bash
   cp .env.example .env
   ```

3. Abra o arquivo .env e configure as seguintes variáveis:

   ```bash
   APP_NAME="your application name"
   DB_DATABASE=your_database_name
   DB_USERNAME=your_database_username
   DB_PASSWORD=your_database_password
   ```

4. Dê permissão de execução ao script start.sh:

   ```bash
   chmod +x start.sh
   ```

5. Execute o script start.sh para iniciar os contêineres e o Laravel:

   ```bash
   ./start.sh
   ```

6. Para começar a desenvolver a aplicação, acesse o contêiner app com o seguinte comando:

   ```bash
   docker compose exec app bash
   ```

## Isso configurará os seguintes serviços:

1. app: PHP-FPM com Laravel   
2. nginx: Servidor web (com SSL habilitado)  
3. mysql: Banco de dados MySQL   
4. redis: Serviço de cache Redis 
5. mailpit: Servidor de e-mail local para desenvolvimento   
6. phpmyadmin: Interface web para gerenciar o banco de dados MySQL   

## Personalização

Você pode personalizar facilmente a configuração do Docker e do Nginx para atender às suas necessidades. Aqui está o que você pode modificar:

- Dockerfile: Modifique para instalar extensões ou ferramentas PHP adicionais.
- nginx/default.conf: Ajuste as configurações e rotas do servidor.
- .env: Altere as variáveis de ambiente para o seu projeto Laravel (por exemplo, credenciais do banco de dados, configurações do Redis).

## Contribuindo

Sinta-se à vontade para contribuir enviando issues ou pull requests. Se você tiver sugestões ou melhorias, elas são sempre bem-vindas!
