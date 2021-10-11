# Ambiente PostgreSQL e pgAdmin 4

## Get started

Install the [Docker](https://www.docker.com/)

Prerequisites

> WSL 2  
> Ubuntu

Then start

Create network and containers, download images if they don't exist yet.

```bash
docker-compose up -d
```

Then stop

```bash
ctrl c
```

Confirm that the postgres-compose-network network was created successfully.

```bash
docker network ls
```

Indicates whether PostgreSQL containers and pgAdmin 4 are running.

```bash
docker-compose ps
```

> In postgres-data you will find the files generated for the volume.

---

### Testing the environment

> Access pgAdmin 4 via the [URL](http://localhost:16543)  
> Enter the access credentials contained in docker-compose.yml

> Creating PostgreSQL instance.  
> Host name/address: inform the name of the container that corresponds to the PostgreSQL instance.
> Port: set the value 5432.  
> Username: O mesmo definido em nome de usuário da instância do PostgreSQL.  
> Password: the same as defined in the PostgreSQL instance password.

> When creating the database, use the same name defined in POSTGRES_DB.

---

### Main commands

    - docker -v: Show docker version
    - docker login: Log in to the docker
    - docker build: create an image from the Dockerfile
    - docker images: List created images
    - docker run: create a container
    - -d: detach, process runs in background
    - docker ps: listed the process running in the Docker
    - docker stop 'container id': stop the container
    - docker start 'container id': start container
    - docker logs 'container id': View container logs
    - docker-compose up: start the service by building the project according to the Dockerfile
    - docker rmi 'container id': stop the container and delete the image
    - docker rm 'container id': remove the container
