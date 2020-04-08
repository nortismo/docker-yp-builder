# docker-yp-builder

This repository contains the Dockerfile used to build the docker-yp-builder container from:

[https://hub.docker.com/r/nortismo/docker-yocto-project-builder](https://hub.docker.com/r/nortismo/docker-yocto-project-builder)

This container can be used to work with Yocto Project. Is is derivated from `ubuntu:19.04` and installs all nessecairy packages to direclty start with Yocto Project. It also creates a build user and adds it to a group called 'faes'. User and groups also need to be existing on the host itself.

## Run with docker-compose

Use following example to derivate a docker-compose.yml for your usecase:

```
version: '3'
services:
  ubuntu:
    image: nortismo/docker-yocto-project-builder
    volumes:
    - /home/build:/home/build
    stdin_open: true
    tty: true
    container_name: 'yocto-container'
```

You can then start the container with `docker-compose up -d` and attach to the bash of the started container with `docker attach <container name>`.