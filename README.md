# PostgreSQL + PGADMIN via Traefik

## Getting started
create .env file with the following content for setting up *initial* username and password.
```
INITIAL_POSTGRES_USER="user"
INITIAL_POSTGRES_PASS="password"
INITIAL_PGADMIN_EMAIL = "user@example.com"
INITIAL_PGADMIN_PASS = "password"
```

Execute for either DEV or PROD environment:
```
docker compose -f ./docker-compose.base.yml -f ./docker-compose.dev.yml up --build --detach
```

or

```
docker compose -f ./docker-compose.base.yml -f ./docker-compose.prod.yml up --build --detach
```

