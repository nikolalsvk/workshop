Crash course on Docker and containers

# What is a container?

A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.


# How are containers built?

In order to create a new container you need to write a definition consisting of instructions containing the steps that need to be executed. For example - install a package, copy a directory from the local machine inside the container and so on. These definitions are called Dockerfiles. I have added an example Dockerfile in this directory - check it out.

# Below you can find several useful commands

# In order to build our container image from the definition we need to run the following command:
docker build -t my-container-name:my-version

# List images on your machine:
docker images

# Download a docker image
docker pull ubuntu:14.04

# Delete an image from your machine:
docker rmi my-image

# run a container:
docker run my-image

# List running containers:
docker ps

# List running containers including failed and completed
docker ps -a

# Stop a container
docker stop my-container

# Remove a container
docker rm my-container

# remove all containers running or stopped (on linux)
docker rm -f $(docker ps -aq)

# view docker cpu/ram usage
docker stats

# Dockerfile reference
https://docs.docker.com/engine/reference/builder/
