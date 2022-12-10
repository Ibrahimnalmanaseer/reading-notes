# Django REST Framework & Docker

## Overview

Docker provides the ability to package and run an application in a loosely isolated environment called a container. The isolation and security allows you to run many containers simultaneously on a given host. Containers are lightweight and contain everything needed to run the application.

## Containers vs Virtual Environments

A virtualenv only encapsulates Python dependencies. A Docker container encapsulates an entire OS.

With a Python virtualenv, you can easily switch between Python versions and dependencies, but you're stuck with your host OS.

With a Docker image, you can swap out the entire OS - install and run Python on Ubuntu, Debian, Alpine, even Windows Server Core.


## Docker architecture


![architecture](https://user-images.githubusercontent.com/62019258/206875814-07f6b8e1-0b58-4a83-820a-a927b56eed54.svg)


## Images and Containers

### Images

 - Firstly define the image with a `Dockerfile`. This is similar to a `Pipenv` or a `requirements.txt` file.

  `$ touch Dockerfile`
  
 - Build image 
 
  `$ docker image build .`
  
  
### Containers

- On the command line, go up a directory to our code folder and create a new one called djangoapp. Then we’ll use Pipenv to install Django and enter the virtual environment shell.

```
$ cd ..
$ mkdir djangoapp && cd djangoapp
$ pipenv install django==3.0
$ pipenv shell

```

### Dockerized Django

- We’ll now create a Dockerfile for our image which will completely replace our local dev environment.

```
$ touch Dockerfile
$ touch docker-compose.yml
```



















