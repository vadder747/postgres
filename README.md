# postgres

* https://hub.docker.com/_/postgres
* https://hub.docker.com/r/dpage/pgadmin4/
* https://www.pgadmin.org/docs/pgadmin4/latest/container_deployment.html

## Run/Stop postgres

```bash
docker compose config
docker compose build

docker compose up -d
docker compose ps
sudo netstat -tulpn | grep LISTEN


docker logs -f mgmt-postgres
docker exec -it mgmt-postgres /bin/bash
psql -h localhost -U postgres -W

docker compose down
docker compose stop

docker image ls
docker image rmi IMAGE
docker pull postgres:latest
```
