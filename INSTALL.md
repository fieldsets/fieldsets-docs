Follow the following 2 steps before starting up the containers.

## 1. DotENV Install
In your `.env` file modify the `COMPOSE_FILE` environment varible so that it follows the variable see in `./env.example`.

- Add `:./src/fieldsets-docs/docker-compose.yml` following `./docker-compose.yml` found at the endof the variable declaration.

## 2. docker-compose.yml Includes
In the top level path of the fieldsets framework, a number of docker compose files exist. Modify the following volume compose file.

#### `docker-compose.volumes.yml`
Add the following line to the end of the include list.
```
- path: ${FIELDSETS_SRC_PATH:-./src/}fieldsets-docs/docker-compose.volumes.yml
    project_directory: ${FIELDSETS_PATH:-./}
    env_file: ${FIELDSETS_PATH:-./}.env
```
