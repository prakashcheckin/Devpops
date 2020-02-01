
1. how to search a docker image in hub.docker.com
```sh
docker search httpd
```

2.  Push image on to dockerhub.cm - docker image can be pushed only with the accont name in prefix
```sh
docker push <image_name>:<image_version/tag>

docker push prakashcheckin/simple-devops-image:latest
```


3. Download a docker image from hub.docker.com
```sh
docker pull <image_name>:<image_version/tag>

docker pull prakashcheckin/simple-devops-image:latest
```

4. List out docker images from your local system
```sh
docker image ls
```

5. Build docker images out of Dockerfile: 

```sh

# -t is a tag name which is image name what we are creating. in below command devps-project is a image name.  last dot mean that dockerfile is available in the current directory.
docker build -t devops-project .

```

4. Create/run/start a docker container from image
```sh

-d is for create container it shoudl run as demon or detached mode. 
docker run -d --name <container_Name> <-p port mapping the port with linux machine port with container port> <image_name>:<image_version/tag>

docker run -d --name devops-container -p 8080:8080 devops-project:latest

```

6. List out running containers
```sh
docker ps 
```

7. List out all docker container (running, stpooed, terminated, etc...)
```sh
docker ps -a
```

9. Stop a container 
```sh
docker stop <container_id>
```

10. Start a container which is in stopped or exit state

```sh
docker start <container_id>
```
11. Remove a container

```sh
docker rm <container_id>
```

11. Remove a image

```sh
docker rmi <image name or id>

# remove images force fully, it remove even the container is present
docker rmi -f <Image_id>
```

12. login to a docker container
```sh
docker exec -it <container_Name> /bin/bash
```
