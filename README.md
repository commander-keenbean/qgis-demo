# QGIS Demo

## QGIS Server

Follow these steps to deploy qgis-server using docker swarm 

1. cd into the server dir

    ```
    cd qgis-server
    ```

2. Build the docker image
    ```
    docker build -f Dockerfile -t qgis-server ./
    ```

3. Deploy the stack
    ```
    docker stack deploy -c qgis-stack.yml qgis-stack
    ```

4. You should see 2 services, nginx and qgis-server
    ```
    docker service ls
    ```

5. Check connection

    ```
    curl localhost
    ```