# PostgreSQL + PGADMIN via Traefik
Traefik is expected to be running as described in [traefik-via-docker-with-sample-services](https://github.com/stopwhispering/traefik-via-docker-with-sample-services).

## Getting started
create `.env` file for setting up *initial* username and password, see. `.example.env` for 
an example.
```
HOSTNAME="example.net" (only required for PROD)
INITIAL_POSTGRES_USER="admin"
INITIAL_POSTGRES_PASS="password"
INITIAL_PGADMIN_EMAIL="admin@example.com"
INITIAL_PGADMIN_PASS="password"
```

Execute for either DEV or PROD environment:
```
docker compose -f ./docker-compose.base.yml -f ./docker-compose.dev.yml up --build --detach
```
or
```
docker compose -f ./docker-compose.base.yml -f ./docker-compose.prod.yml up --build --detach
```

## Accessing the services
- PostgreSQL: `http://postgres-db.localhost:5432` or `https://postgres-db.example.net:5432` or `postgres-db:5432` (docker-internally)
- PGADMIN: `http://pgadmin.localhost` or `https://pgadmin.example.net`
