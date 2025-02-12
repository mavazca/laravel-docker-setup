# Laravel Docker Setup
O objetivo desse repositorio é fornecer uma configuração rápida e fácil para iniciar um projeto Laravel com Filament, utilizando containers dockers que pode ser utilizado em ambientes de desenvolvimento e produção.

## Pré-requisitos
Antes de começar, certifique-se de ter o seguinte instalado:

- Docker
- Docker Compose

## Funcionalidades
- Laravel 12
- FilamentPHP
- PHP 8.4
- Nginx
- FrankenPHP
- Swoole
- MySQL
- PhpMyAdmin
- Redis
- Mailtip
- Composer
- NPM

## Instalação
Para começar com este projeto, siga estas etapas:

1. Clone este repositório:

   ```bash
   git clone https://github.com/mavazca/laravel-docker-setup && cd laravel-docker-setup
   ```

2. Copie o arquivo .env.example para .env

   ```bash
   cp .env.example .env
   ```

3. Abra o arquivo .env e configure as seguintes variáveis:

   ```bash
   APP_NAME=Laravel
   DB_DATABASE=
   DB_USERNAME=
   DB_PASSWORD=
   ```

4. Dê permissão de execução aos scripts:

   ```bash
   chmod +x install 
   ```

5. Execute o script install para instalar um novo projeto Laravel com FilamentPHP com servidor de aplicação desejado (FrankenPHP, Swoole ou Nginx), você pode usar as seguintes opções:
    - --frankenphp (-f)
    - --swoole (-s)
    - --nginx (-n)
    - --build (-b) 

   ```bash
   ./install --frankenphp
   ```

   Instalar o projeto e reconstruir as imagens, use o seguinte comando:
   ```bash
   ./install --frankenphp --build
   ```

6. Comandos para executar no projeto:

    Iniciar os containers:
   ```bash
   docker compose up -d
   ```
   Parar os containers:
   ```bash
   docker compose down
   ```
   Acessar o container app:
   ```bash
    docker compose exec app bash
    ```

## Parabéns
Instalação concluída com sucesso!

### Acessar o projeto no link: [http://localhost/admin](http://localhost/admin).

    - Usuário: test@example.com
    - Senha: password

### Acessar o phpMyAdmin no link: [http://localhost:8080](http://localhost:8080).

    - Usuário: root
    - Senha: root

## Contribuição
Contribuições são bem-vindas! Se você encontrar algum problema ou tiver sugestões de melhorias, sinta-se à vontade para abrir uma issue ou enviar um pull request.
