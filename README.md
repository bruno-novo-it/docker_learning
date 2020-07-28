# docker_learning
This repository was created to increase and help the learning path of developing microservices applications


## Docker Commands

```
docker ps # List running Containers
```

docker ps -a

docker images

docker logs -f CONTAINER_ID

docker-compose up -d

docker-compose down




docker build -t my_docker_flask .

docker run -it --name my_docker_flask -p 5000:5000 my_docker_flask

docker run -it --name my_docker_flask my_docker_flask Wrong


docker rm -f $(docker ps -qa)

docker rmi -f $(docker images -f "dangling=true" -q)

docker rmi -f $(docker images)