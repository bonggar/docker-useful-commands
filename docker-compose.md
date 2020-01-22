Terminal into docker container
- `docker exec -it :container_id bash`
or
- `docker-compose run [service] bash`

Validate the compose file
- `docker-compose config`

Run the docker container in debug mode
- `docker-compose run --service-ports web`

Build the docker container
- `docker-compose build`

Start the docker container
- `docker-compose up`

Start the docker container and run in the backgroud process (daemon)
- `docker-compose up -d`

Remove all docker containers in the repository
- `docker-compose down`

Remove a specific docker container
- `docker kill :container_id`

Scale Services
- `docker-compose scale [SERVICE=NUM...]`
ex: `docker-compose scale server=3 web=2`
