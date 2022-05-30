# docker-getting-started

https://docs.docker.com/get-started/

## Notes

```sh
# to create the docker image
docker build -t getting-started .

# To see current running containers
docker ps

# to stop a running container
docker stop <ContainerID>

# to remove a stopped container
docker rm <ContainerID>

# to run a container using image<getting-started> in detach mode and exposing port 3000
docker run -dp 3000:3000 getting-started


docker run -dp 3000:3000 \
-w /app -v "$(pwd):/app" \
node:12-alpine \
sh -c "yarn install && yarn run dev"
```