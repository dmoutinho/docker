# Testing Image Layer


1- Pull a Docker image:
```sh
$ docker pull alpine
```

2- Run a Docker image in iterative mode:
```sh
$ docker run -it alpine
```

3- Create a file:
```sh
$ touch /home/new-file.txt && exit
```

4- Show the container id:
```sh
$ docker ps -a
```

5- Commit the container id:
```sh
$ docker commit CONTAINER_ID
```

6- Show the new image id:
```sh
$ docker images
```

7- Tag the new image id:
```sh
$ docker tag IMAGE_ID dmoutinho/new-alpine
```

8- Push a new image to registry:
```sh
$ docker push dmoutinho/new-alpine
```

9- Delete a new image:
```sh
$ docker image rm dmoutinho/new-alpine
```

10- Run a new image:
```sh
$ docker run -it dmoutinho/new-alpine
```

11- List files:
```sh
$ ls /home && exit
```
