# PostgreSQL/PostGIS & pgAdmin with docker-compose

## Requirements:

- docker >= 18.02.0+

## Quick Start

- clone this repository
- `$ cd path/to/cloned/repo/`
- run `docker-compose up -d`

`PGDATA` is mounted locally in [volumes/pgdata](./volumes/pgdata) and contains the database files.
`pgadmin` is mounted locally in [volumes/pgadmin](./volumes/pgadmin) and contains the pgadmin session configuration files.

## Environment variables

The docker-compose file has the following environment variables:

- `POSTGRES_USER` the default value is **postgres**
- `POSTGRES_PASSWORD` the default value is **SuperSecret**
- `PGADMIN_DEFAULT_EMAIL` the default value is **pgadmin@pgadmin.org**
- `PGADMIN_DEFAULT_PASSWORD` the default value is **SuperSecret**
- `PGADMIN_LISTEN_PORT` the default value is **49152**

## Usage

### Access to pgAdmin:

- **URL:** [`http://localhost:49152`](http://localhost:49152) (by default)
- **Username:** `pgadmin@pgadmin.org` (by default)
- **Password:** `SuperSecret` (by default)

### Configure postgres within pgAdmin:

- **Host name/address** `postgres`
- **Port** `5432`
- **Maintenance database** `postgres`
- **Username** as `POSTGRES_USER`, by default: `postgres`
- **Password** as `POSTGRES_PASSWORD`, by default `SuperSecret`

### Shutdown

- run `$ docker-compose down` from the directory hosting the docker-compose file

### More

For more detailed instructions about how to start and control your Postgres container, see the documentation for the postgres image [here](https://registry.hub.docker.com/_/postgres/).

## Resources

- docker image postgis : https://registry.hub.docker.com/r/postgis/postgis
- docker image for postgres : https://registry.hub.docker.com/_/postgres/
- additional pgAdmin configuration : https://www.pgadmin.org/docs/pgadmin4/latest/container_deployment.html

## License

Licensed under the MIT License

A copy of the license is available in the repository's [LICENSE](LICENSE) file.
