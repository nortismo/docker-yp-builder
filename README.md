# docker-yp-builder

This repository contains the Dockerfile used to build the docker-yp-builder container from:

[https://hub.docker.com/r/nortismo/docker-yocto-project-builder](https://hub.docker.com/r/nortismo/docker-yocto-project-builder)

This container can be used to work with Yocto Project. Is is derivated from `ubuntu:19.04` and installs all nessecairy packages to direclty start with Yocto Project. It also creates a build user and adds it to a group called 'faes'. User and groups also need to be existing on the host itself.