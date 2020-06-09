
## Docker image for Alpine with Firefox
[![Docker Image Size (tag)](https://img.shields.io/docker/image-size/hex0cter/alpine-firefox/latest)](https://hub.docker.com/r/hex0cter/alpine-firefox)
[![Docker Cloud Automated build](https://img.shields.io/docker/cloud/automated/hex0cter/alpine-firefox)](https://hub.docker.com/r/hex0cter/alpine-firefox/builds)
[![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/hex0cter/alpine-firefox)](https://hub.docker.com/r/hex0cter/alpine-firefox/builds)
[![Docker Pulls](https://img.shields.io/docker/pulls/hex0cter/alpine-firefox)](https://hub.docker.com/r/hex0cter/alpine-firefox)

This image allows you to run the ***Firefox*** browser inside a docker container. For Chrome please click [here](https://github.com/hex0cter/alpine-chrome).

## What is included?
* alpine with X server (use `DEBUG=true` to turn on the vnc server)
* nodejs
* yarn
* firefox
* docker-cli (in case you want to run some automated tests against services running from another container, with ***/var/run/docker.sock*** mounted)

## Pull the image
```bash
docker pull hex0cter/alpine-firefox:latest
```
Please visit [docker hub](https://hub.docker.com/repository/docker/hex0cter/alpine-firefox) for more details.

## Start a container
```bash
docker run -it --rm hex0cter/alpine-firefox firefox
```

## Debug mode
```bash
docker run -it --rm -e DEBUG=true -p 5900:5900 hex0cter/alpine-firefox firefox
```
When **DEBUG=true**, the VNC server will be started, so you can access the container's GUI from any VNC viewer (port 5900).
