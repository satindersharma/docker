# docker



#### `docker ps`

#### `docker-compose -f docker-compose-staging.yml up -d`
above -f is look for this specific file(as default is docker-compose.yml)


#### to up a specific services (this will make a look at the services in docker-compose.yml file)
#### `docker-compose up mysql -d`

#### open bash in the container
#### docker ps (to see the container `NAMES`), then
#### `docker exec -it CONZATINDER_NAME bash`

#### To see the logs
`docker logs CONTANER_NAME`

---
### All images

#### `docker image ls`

---
## To list services

### `docker compose ps`
##### -f flag let specify custom docker  compose yml (by default it is `docker-compose.yml`)

### `docker compose -f docker-compose-staging.yml ps`

---

### To restart

#### `docker-compose restart mysql`
#### `docker compose -f docker-compose-staging.yml restart`

#### `docker compose -f docker-compose-staging.yml restart crawler-api`




### Always check for the docker oficial image with an alpine version https://hub.docker.com/

#### `image:[version number]-alpine` or `image:tag`

#### `docker pull python:3.10` has a size of 867 MB
### but 
#### `docker pull python:3.10-alpine`  has a size of 48 MB

#### to run directly

### `docker run -it --rm python:3.10-alpine`



### `docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres:13-alpine`
### `docker run --name postgresql_container_name -e POSTGRES_USER=myusername -e POSTGRES_PASSWORD=mypassword -p 5432:5432 -v /data:/var/lib/postgresql/data -d postgres:13-alpine`

### get into bash of container
### `docker exec -it postgresql_container_name bash`
### Login with user and pasword
### `psql -U myusername`
### `CREATE DATABASE dbname;`
### to see db
### `\l`

