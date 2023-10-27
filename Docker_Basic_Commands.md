- [Docker\_Basics](#docker_basics)
  - [Install Docker](#install-docker)
  - [Docker Installations](#docker-installations)
  - [Verify Docker version and also login to Docker Hub](#verify-docker-version-and-also-login-to-docker-hub)
  - [Pull image and verify](#pull-image-and-verify)
  - [Docker basic commands](#docker-basic-commands)
    - [List Running Containers](#list-running-containers)
    - [Connect to Container Terminal](#connect-to-container-terminal)
    - [Container Stop, Start](#container-stop-start)
    - [Remove Container](#remove-container)
    - [Remove Image](#remove-image)



# Docker_Basics
Basics of Docker

## Install Docker

## Docker Installations
- https://docs.docker.com/install/

- Windows - https://docs.docker.com/docker-for-windows/
- MAC - https://docs.docker.com/docker-for-mac/


## Verify Docker version and also login to Docker Hub
```
docker version
docker login
```

## Pull image and verify
docker pull muthu4all/php_app_color:maroon

docker run --name my_first_app -p 80:80 -d muthu4all/php_app_color:maroon

## Docker basic commands

### List Running Containers
```
docker ps
docker ps -a
docker ps -a -q
```

### Connect to Container Terminal
```
docker exec -it <container-name> /bin/sh
```
**Note** - Inside the shell following command to executed to confirm its container shell.
```
hostname
pwd
```
**Note** - 'exit' to come out of the container


### Container Stop, Start 
```
docker stop <container-name>
docker ps
docker start  <container-name>
docker ps
```

### Remove Container 
```
docker stop <container-name> 
docker ps -a
docker rm <container-name>
docker ps -a

```

### Remove Image
```
docker images

docker rmi  <image-id>
or 
docker rmi  <image-name>

docker rmi muthu4all/php_app_color:maroon
```

**Note** - Instead of image id, image name can be used. While using the image name, tag should be added. By default tag with 'latest' tag will be considered.