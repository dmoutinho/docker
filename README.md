

# Docker

## Container

>A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.

[Docker - What Container](https://www.docker.com/resources/what-container)

## Container x Virtual Machines

## Setting Up Docker on VM

### Setting Up VM

- Download [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- Download Linux image [CentOS-7-x86_64-Minimal-1810.iso](http://isoredirect.centos.org/centos/7/isos/x86_64/CentOS-7-x86_64-Minimal-1810.iso)
- Install VirtualBox and run
- Create a VirtualBox image
    - New
    - Name: Docker/ Type: Linux/ Type: Ubuntu 64-bit [Next]
    - Memory size: 1024MB [Next]
    - Create a virtual hard disk now [Next]
    - VDI [Next]
    - Dynamically allocated [Next]
    - Size 50GB [Next]
    - [Create]
- Run Docker image
    -  Select Docker and start
    -  In the first time, select the .iso file to install the OS
    -  After the OS load, click "Install Linux" in Desktop
- Load OS
- Update Repository
```sh
$ su yum update
```

### Setting Up Docker
https://docs.docker.com/install/linux/docker-ce/centos/

```sh
$ sudo yum install -y yum-utils \
  device-mapper-persistent-data \
  lvm2
```
```sh
$ sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo
```
```sh
$ sudo yum install docker-ce
```
```sh
$ sudo systemctl start docker
```
```sh
$ sudo docker run hello-world
```

https://docs.docker.com/install/linux/linux-postinstall/

```sh
$ sudo groupadd docker
$ sudo usermod -aG docker $USER
```
```sh
$ sudo systemctl enable docker
```
### Docker Compose
### Common Commands
