# postgres

* [postgres](https://hub.docker.com/_/postgres)
* [pgadmin4](https://hub.docker.com/r/dpage/pgadmin4/)
* [pgAdmin - Container Deployment](https://www.pgadmin.org/docs/pgadmin4/latest/container_deployment.html)

## Run/Stop postgres

```bash
docker compose config
docker compose -f docker-compose-gold-srv1.yml config
docker compose build
docker compose build --no-cache
docker compose -f docker-compose-gold-srv1.yml build
docker compose -f docker-compose-gold-srv1.yml build --no-cache

docker compose up -d
docker compose -f docker-compose-gold-srv1.yml up -d
# Up pgadmin4
docker compose -f docker-compose-gold-srv1.yml up -d pgadmin4
docker compose ps
docker compose -f docker-compose-gold-srv1.yml ps

docker compose down
docker compose -f docker-compose-gold-srv1.yml down
# Down pgadmin4
docker compose -f docker-compose-gold-srv1.yml down pgadmin4
docker compose stop
docker compose -f docker-compose-gold-srv1.yml stop

docker logs -f mgmt-postgres
docker logs -f gold-srv1-postgres
docker exec -it mgmt-postgres /bin/bash
docker exec -it gold-srv1-postgres /bin/bash

psql -h localhost -U postgres -W
```

## Various

```bash
netstat -tulpn | grep LISTEN
nmap localhost

docker container ls -a
docker container prune

docker image ls -a
# Remove unused images
docker image prune
docker image prune -a

docker image ls
# Remove one or more images
docker image rmi IMAGE

# Download an image from a registry
docker pull postgres:latest
docker pull postgres:14.15

docker network ls
docker network prune
```
