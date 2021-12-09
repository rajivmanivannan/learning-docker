
## The following execise is to demonstrate how to create your own docker image, run and publish it in the Docker Hub. 

### To demonstrate I create an Image which has a single page static website which runs in the Nginx web server.

### Install Docker in your machine
```
$ brew cask install docker
$ brew cask install virtualbox
```
### Create account and login into Docker Hub

Open a account here https://hub.docker.com </br>
Create a repostitory named "static-site"</br>
```
$ docker login
```
### Copy the files in the static-site folder to your local folder

### Provide permission to execute
```
$ chmod +x wrapper.sh
```
### Build a docker image “static-site”
```
$ docker build -t static-site .
```
### To view the list of images in the docker
```
$ docker images
```
### To tag a docker image
```
$ docker tag a3e4634f6d1d <DockerHubId>/static-site:latest
```
### To push the docker image to docker hub:
```
$ docker push <DockerHubId>/static-site
```
### To run the docker image in the available port:
```
$ docker run -d -P --name static-site <DockerHubId>/static-site:latest
```
### To see the port assigned to your container
```
$ docker port static-site
```
### To run the image with specified port:
```
$ docker run -p 8888:80 <DockerHubId>/static-site
```
### To see the result
```
http://localhost:8888
```
### To stop all docker container: 
```
$ docker stop $(docker ps -a -q)
```
### To remove all docker container:
```
$ docker rm $(docker ps -a -q)
```
### To remove docker image:
```
$ docker rmi <DockerHubId>/static-site:latest
```
