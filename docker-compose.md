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

# Run [Bday](https://github.com/dmoutinho/bday-alert) App
<p align="center">
  <img src="https://docs.google.com/drawings/d/e/2PACX-1vSzTCFgX_-1e3cJzBIF8zihhGvvZhHPHad0rp6Ep8PFB2K7REnZa453XVBiY9celLDgKvL8M8oIupkh/pub?w=553&h=275">
</p>

1- Copy [docker-compose.yml](https://github.com/dmoutinho/docker/blob/master/docker-compose.md#compose-file):
```sh
$ curl https://raw.githubusercontent.com/dmoutinho/docker/master/docker-compose.yml > docker-compose.yml
```

2- Run [docker-compose.yml](https://github.com/dmoutinho/docker/blob/master/docker-compose.md#compose-file):

```sh
$ docker-compose up
```

3- Check [docker-compose.yml](https://github.com/dmoutinho/docker/blob/master/docker-compose.md#compose-file):

```sh
$ docker-compose ps
```

4- Stop [docker-compose.yml](https://github.com/dmoutinho/docker/blob/master/docker-compose.md#compose-file):

```sh
$ docker-compose down
```

# Compose file
<p align="center">
  <img src="https://docs.google.com/drawings/d/e/2PACX-1vRJ2zG7IYAzzyC14RtIqQxVm4tSeqD6yzPD_ea4pCJLP12-B4W6yFeD6WplrBQEX2hLfouvqHKU-bRN/pub?w=579&h=693">
</p>



