## Run this following command.
### Lab 1
1. Change directory to lab_1
    ```sh
    cd lab_1
    ```
2. Build
    ```sh
    docker build -t hello-world .
    ```
3. Verify Image
    ```sh
    docker images | grep hello-world
    docker images | findstr hello-world
    ```
4. Run
    ```sh
    docker run --name hello-container hello-world
    ```
5. Verify docker process
    ```sh
    docker ps -a | grep hello-container
    docker ps -a | findstr hello-container
    ```
### Lab 2
1. Change directory to "simple-golang-api"
2. Modify Dockerfile and add compose file
3. Use Docker compose to build
    ```sh
    docker compose up --build --detach
    ```
4. Use Docker compose to verify process
    ```sh
    docker compose ps
    ```
5. Use Docker compose to stop container
    ```sh
    docker compose down
    ```