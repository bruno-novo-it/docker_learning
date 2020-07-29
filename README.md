# docker_learning
This repository was created to increase and help the learning path of developing microservices applications


## Docker Commands

```
# Run Nginx Container
docker run --name nginx -d -p 8080:80 nginx

# Run Ubuntu Container
docker run -it ubuntu bash

# List running Containers
docker ps

# List Stopped/Exited Containers
docker ps -a

# List Local Docker Images
docker images

# Show Container's log's
docker logs -f CONTAINER_ID

# Build a docker Image
docker build -t CONTAINER_NAME .

# Run a docker image
docker run -it --name CONTAINER_NAME CONTAINER_IMAGE

# Run a docker image with port argument
docker run -it --name CONTAINER_NAME -p LOCAL_PORT:CONTAINER_PORT CONTAINER_IMAGE

# Run multiple contaienr images in background
docker-compose up -d

# Stop multiple contaienr images in background
docker-compose down

# Remove all Running and Stopped Container's
docker rm -f $(docker ps -qa)

# Remove all Unneused Docker images
docker rmi -f $(docker images -f "dangling=true" -q)

# Remove all Local docker Images
docker rmi -f $(docker images)
```