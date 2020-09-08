# [OBMIN Server](https://obmin.github.io) [<img alt="OBMIN" src="obmin.svg" align="right"  style="margin:0">](https://github.com/konkor/obmin)

![Build Status](https://travis-ci.com/konkor/obmin-docker.svg?branch=master)

A secure private personal server for your data.

## Usage
_You should use **obmin** id for the git version and **obmin/obmin** for dockerhub versions._

## Building the docker image
```sh
docker build -t obmin .
```

### Running the obmin container
```sh
docker run --rm --volume="$PWD:/srv/obmin" -p 80:8088 -it obmin
```

### Use **-d** option to run a container in background

```console
$ docker run -d --rm --volume="$PWD:/srv/obmin" -p 80:8088 -it obmin
```
### Running the server with custom arguments
```sh
docker run --rm --volume="$PWD:/srv/obmin" -p 80:8088 -it obmin obmin-server --config /etc/obmin.config
```

## Using Dockerhub images
### Pulling the obmin container from dockerhub
```sh
docker pull obmin/obmin
```

### Running the dockerhub obmin container
```sh
docker run --rm --volume="$PWD:/srv/obmin" -p 80:8088 -it obmin/obmin
```

## Customizing
1. Modify `obmin.config`.
2. Build image.
