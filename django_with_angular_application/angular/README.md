### How to run and/or create a new projet(locally)

To work with Angular, we need to install npm, the node package manager
[Clique aqui para mais informações de como instalar(Ubuntu)](https://www.hostinger.com.br/tutoriais/instalar-node-js-ubuntu/)
[Clique aqui para mais informações de como instalar(MacOSX)](https://treehouse.github.io/installation-guides/mac/node-mac.html)

To create a new project using Angular, just execute the following steps:
```
npm install -g @angular/cli # Will install the Angular Client in you machine

ng new frontend

cd frontend

ng serve
```

### How to build and run a container with the application

To create a container with the create code, create and/or edit the `Dockerfile` file and run:
```
docker build -t frontend .
```

This will `BUILD` and Docker Image with all the dependencies we need and with our application inside.

To `RUN` this image, just execute:
```
docker run -d -it --name frontend -p 4200:4200 frontend:latest
```

To access, just go to --> http://localhost:4200