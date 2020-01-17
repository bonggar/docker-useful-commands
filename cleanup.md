Stop all containers:
- `docker ps -aq | xargs docker stop`

Remove all containers: 
- `docker ps -aq | xargs docker rm`

Remove all images: 
- `docker images -aq | xargs docker rmi`

Remove all networks: 
- `docker network ls -q | xargs docker network rm`

Remove all volumes: 
- `docker volume ls -q | xargs docker volume rm`

Remove all stopped containers, unused networks, dangling images, and build cache:
- `docker system prune`
