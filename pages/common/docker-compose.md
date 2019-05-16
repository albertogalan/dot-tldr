# docker-compose

> Run and manage multi container docker applications.

- Create and start all containers in the background using a docker-compose.yml file from the current directory:

`docker-compose up -d`

- Start all containers, rebuild if necessary:

`docker-compose up --build`

- Start all containers using an alternate compose file:

`docker-compose --file {{path/to/file}} up`

- Stop all running containers:

`docker-compose stop`

- Stop and remove all containers, networks, images, and volumes:

`docker-compose down`

- Follow logs for all containers:

`docker-compose logs --follow`


- See logs of docker compose

`docker-compose logs --tail 5 -f CONTAINER_NAME`


- Run psql inside container

`docker-compose exec postgres psql -Upostgres`


- Recretate database

`docker-compose down`
`sudo rm -rf docker-volumes/postgres-data`
`docker-compose up`

