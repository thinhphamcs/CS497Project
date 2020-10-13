# CS497Project

## Application structure

![Alt text](img/microservice-architecture.png)

This application consists of 5 different micro-services which are Accounts, Submission Testing, Submission History, Challenges and Gateway/Sessions. The subdirectory for each micro-service contains the source code and documentation to run each service independently if one chooses to do so. The documentation also contains information about various endpoints that each API has.

## Running the project

Prerequisites: [docker](https://docs.docker.com/engine/install/) and [docker-compose](https://docs.docker.com/compose/install/)

1. Checkout files with `git clone https://github.com/jitli98/CS497Project.git && cd CS497Project`

2. Build and run all services with `docker-compose up --build`

3. The host name and ports of each service are as follows: \
    Exemplar:
    ```
     http://0.0.0.0:3000/
    ```
    Accounts:
    ```
     http://0.0.0.0:4000/
    ```
    Challenges:
    ```
     http://0.0.0.0:5000/
    ```
    Sessions:
    ```
     http://0.0.0.0:6000/
    ```
    Submission History:
    ```
     http://0.0.0.0:7000/
    ```
    Submission Testing:
    ```
     http://0.0.0.0:8000/
    ```

<hr>

### To perform a CLEAN restart of Docker Instances:
1. Stop the container(s) using the following command:
    ```
    docker-compose down
    ```
2. Delete all containers using the following command:
    ```
    docker rm -f $(docker ps -a -q)
    ``` 
3. Delete all volumes using the following command(Only do this if you intend on removing persistent data stored in volumes):
    ```
    docker volume rm $(docker volume ls -q)
    ``` 
4. Restart the containers using:
    ```
    docker-compose up --build
    ```

