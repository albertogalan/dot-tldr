# docker

> Manage Docker containers and images.

- List currently running docker containers:

`docker container ls`

- List all docker containers (running and stopped):

`docker container ls -a`

- Start a container:

`docker container start {{container}}`

- Stop a container:

`docker container stop {{container}}`

- Start a container from an image and get a shell inside of it:

`docker container run -it {{image}} bash`

- Run a command inside of an already running container:

`docker container exec {{container}} {{command}}`

- Remove a stopped container:

`docker container rm {{container}}`

- Fetch and follow the logs of a container:

`docker container logs -f {{container}}`
- push image docker
`docker login agalan75 ` 
`NAME=name && docker build -t agalan75/$NAME .  && docker push agalan75/$NAME`


- login into quay.io

`docker login quay.io`


- Create persistent volume

`docker volume create --name nexus-data`
`docker run -d  --name nexus -v /some/dir/nexus-data:/nexus-data  sonatype/nexus3`


