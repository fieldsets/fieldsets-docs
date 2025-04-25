Follow the following 2 steps before starting up the containers.

## Dotenv Install
In your `.env` file modify the `COMPOSE_FILE` environment varible so that it follows the variable see in `./env.example`.

- Add `:./src/fieldsets-docs/docker-compose.volumes.yml` following `./docker-compose.volumes.yml` found towards the beginning of the variable declaration.
- Add `:./src/fieldsets-docs/docker-compose.yml` following `./docker-compose.yml` found at the endof the variable declaration.

## Deployment

Deployment utilizes Mkdocs internal githup page deployment functionality.