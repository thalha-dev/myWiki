# DOCKER

#### WHY?
>Hard time deployment and many more

### Docker Architecture
![image showing architecture of docker](https://docs.docker.com/engine/images/architecture.svg)

### Downloading Image

Docker image can be downloaded from any registry. Docker Hub is the default registry.

> docker pull IMAGE_NAME:TAG_NAME

### Running Docker Image

Docker image can be use to create new container, using run command.

> docker run IMAGE_NAME

* `docker run image command` will create a comtainer from the image and run the command and exit the container once the command gets fully executed. 
* `docker run -i -t image` will create a comtainer from the image and expose the STDIN, STDOUT and STDERR on host machine.
* `docker run` will always create a new container with given image.
* `exit` command will stop the container.

*options* 
* -i --> interactive
* -t --> allocate pseduo tty
* -d --> detach
* -p --> mention port like HostPort:ContainerPort

### Start and attach to existing container

> docker start IMAGE_NAME/IMAGE_ID   
> docker attach IMAGE_NAME/IMAGE_ID

* attaching before starting will not work

### Listing Images and Containers

* `docker images` or `docker image ls` will list available images in the host machine.
* `docker ps` will list running container in the host machine.
* `docker ps -a` (-a for all) will list running container as well as stopped containers in the host machine.

### Giving Name To New Container

* `docker run --name <givename> IMAGE`

### To Stop a Running Container

*  `docker stop <ID>/name`, it will take some time to actually stop the container.
*  `docker kill <ID>/name`, it will immediately stop the container.

### To Get the Logs of running container in host terminal

*  `docker logs -f --tail <number>`, it will log the container's output to host terminal.

*options* 
* -f --> follow
* --tail or -n --> tail lines to show


