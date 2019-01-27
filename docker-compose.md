# Docker Compose

>Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services. Then, with a single command, you create and start all the services from your configuration. To learn more about all the features of Compose, see the [list of features](https://docs.docker.com/compose/overview/#features).

# [Install Docker Compose](https://docs.docker.com/compose/install/)

1- Run this command to download the 1.23.2 version of Docker Compose:

```sh
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-Linux-x86_64" -o /usr/local/bin/docker-compose
```

2- Apply executable permissions to the binary:

```sh
$ sudo chmod +x /usr/local/bin/docker-compose
```

3- Test the installation.

```sh
$ docker-compose --version
```
