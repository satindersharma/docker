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

