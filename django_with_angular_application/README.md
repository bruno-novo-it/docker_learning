#### Shopping List with Django(Backend and Angular(Frontend))

##### How to run the Application

Just execute:
```
docker-compose up -d
```

Will build all the images we need(Django and Angular).
After that, just go to: http://localhost:4200.

To access the Backend, go to: http://localhost:8000



##### Usefull Docker Commands

**`docker ps`** --> Show all runnin containers.
**`docker ps -a`** --> Show all running and stopped container.
**`docker images`** --> Show all you docker images.

**`docker build -t blabla .`** --> Will **BUILD** a new docker image with called *blabla*.

**`docker run -it --name my_first_docker_container blabla:latest`** --> Will execute the image you created and put the name `my_first_docker_container` to it.

**`docker rm -f <ID or NAME>`** --> will remove a running container, by it's `ID` ou by it's `NAME`.

**`docker rmi -f <ID or NAME>`** --> Will remove a docker image from your list of images, by it's `ID` or by it's `NAME`.

**`docker rmi $(docker images -f "dangling=true" -q)`** --> Will remove all untagged container images from the list

**` docker rm -f $(docker ps -a -q)`** --> Will remove **ALL** you **Running** and **Stopped** container