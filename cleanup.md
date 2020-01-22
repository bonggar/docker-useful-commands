### System

Remove all stopped containers, unused networks, dangling images, and build cache:
- `docker system prune`

If you also want to remove all unused volumes, pass the --volumes flag:
- `docker system prune --volumes`

### Containers

Stop all containers:
- `docker stop $(docker ps -a -q)`
or
- `docker ps -aq | xargs docker stop`

Remove all containers: 
- `docker ps -aq | xargs docker rm`
or
- `docker rm $(docker ps -a -q)`

Remove all stopped containers: 
- `docker container prune`

Remove all stopped containers using filter (ex: created more than 12hours ago): 
- `docker container prune --filter "until=12h"`

Stop and Remove all container
- `docker container stop $(docker container ls -aq)`
- `docker container rm $(docker container ls -aq)`

### Images

Remove all images: 
- `docker images -aq | xargs docker rmi`
or
- `docker rmi $(docker images -q)`

Remove dangled and unused images (an image that is not tagged and is not used by any container)
- `docker image prune`

Remove all unused images: 
- `docker image prune -a`

Remove all images using filter (ex: created more than 12hours ago): 
- `docker image prune -a --filter "until=12h"`

### Networks

Remove all networks: 
- `docker network ls -q | xargs docker network rm`

Remove all unused network
- `docker network prune`

Remove all networks using filter (ex: created more than 12hours ago):
- `docker network prune -a --filter "until=12h"`

### Volumes

Remove all volumes: 
- `docker volume ls -q | xargs docker volume rm`

Remove all unused volumes
- `docker volume prune`

