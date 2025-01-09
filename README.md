## Run this following command.
### Lab 1
- cd lab_1
- docker build -t hello-world .
- docker images | grep hello-world
- docker run --name hello-container hello-world 
- docker ps --a | grep hello-container
### Lab 2
- cd lab_2 
- docker compose up --build
- docker compose ps
- docker compose down