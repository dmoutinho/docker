# Docker

> Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.

> Docker provides the ability to package and run an application in a loosely isolated environment called a [**container**](https://github.com/dmoutinho/docker#container). The isolation and security allow you to run many containers simultaneously on a given host. Containers are lightweight because they don’t need the extra load of a hypervisor, but run directly within the host machine’s kernel. This means you can run more containers on a given hardware combination than if you were using virtual machines. You can even run Docker containers within host machines that are actually virtual machines!

[Docker - Overview](https://docs.docker.com/engine/docker-overview/)

Docker uses features of Linux kernel:
- **Namespaces**: each resource (Pid, Network,  InterProcess Communication, Mount, Unix Timesharing System) of a container runs in an isolated area.
- **Control groups**: limits an application to a specific set of resources.
- **Union file systems**: are file systems that operate by creating layers, making them very lightweight and fast.

[Docker - Overview](https://docs.docker.com/engine/docker-overview/)

Docker is a set of technologies, for example:
- **Docker Engine**: a daemon for creating and executing [Docker image](https://github.com/dmoutinho/docker#docker-image).
- [Docker Hub](https://hub.docker.com/u/dmoutinho): a public registry for Docker image.
- [Docker Compose](https://github.com/dmoutinho/docker/blob/master/docker-compose.md): a tool for defining and running multi-container Docker applications. 

![N|Solid](https://docs.docker.com/engine/images/architecture.svg)
[Docker - Architecture](https://docs.docker.com/engine/docker-overview/)

## Container

>A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.
[Docker - What Container](https://www.docker.com/resources/what-container)

## Docker Image
Docker image is created in layers and these layers are used to create other images. This way makes the push / pull more efficient in the registry. [Testing Image Layer](https://github.com/dmoutinho/docker/blob/master/image-layer.md) and 
[Creating Image](https://cloud.docker.com/repository/docker/dmoutinho/bday-alert/general).

## Container x Virtual Machines

## Setting Up Docker on VM

### Setting Up VM

- Download [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- Download Linux image [CentOS-7-x86_64-Minimal-1810.iso](http://isoredirect.centos.org/centos/7/isos/x86_64/CentOS-7-x86_64-Minimal-1810.iso)
- Install VirtualBox and run
- Create a VirtualBox image
    - New
    - Name: Docker/ Type: Linux/ Type: Red Hat 64-bit [Next]
    - Memory size: 1024MB [Next]
    - Create a virtual hard disk now [Next]
    - VDI [Next]
    - Dynamically allocated [Next]
    - Size 50GB [Create]
- Run Docker image
    -  Select Docker and start
    -  In the first time, select the .iso file to install the OS
    -  After the OS load, choose "Install CentOS 7"
- Load OS
- Update Repository
```sh
$ su yum update
```

### [Setting Up Docker](https://docs.docker.com/install/linux/docker-ce/centos/)

1- Install required packages.
```sh
$ sudo yum install -y yum-utils \
  device-mapper-persistent-data \
  lvm2
```

2- Use the following command to set up the stable repository.
```sh
$ sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo
```

3- Install the latest version of Docker CE
```sh
$ sudo yum install docker-ce
```

4- Start Docker.
```sh
$ sudo systemctl start docker
```

5- Verify that docker is installed correctly by running the hello-world image.
```sh
$ sudo docker run hello-world
```

### [Setting Up Docker Post-installation](https://docs.docker.com/install/linux/linux-postinstall/)

1- Create/add user to the docker group
```sh
$ useradd docker -g docker
```

2- Configure Docker to start on boot
```sh
$ sudo systemctl enable docker
```

## Common Commands

- **docker images**: list images.
- **docker pull IMAGE_NAME**: pull an image or a repository from a registry.
- **docker push IMAGE_NAME**: push an image or a repository from a registry.
- **docker build -t IMAGE_NAME .**:  build an image from a Dockerfile.
- **docker tag SOURCE_IMAGE TARGET_IMAGE**: create a tag TARGET_IMAGE that refers to SOURCE_IMAGE.
- **docker ps**: list containers running.
- **docker ps -a**: list containers.
- **docker run -it IMAGE_NAME**: run container in iterative mode.
- **docker start CONTAINER_ID**: start container.
- **docker stop CONTAINER_ID**: stop container.
- **docker rm CONTAINER_ID**: remove container.
- **docker container prune**: remove all stopped containers.
- **docker rmi IMAGE_NAME**: remove image.

## References

[Docker Documentation](https://docs.docker.com/)

[Play with Docker Classroom](https://training.play-with-docker.com/)
