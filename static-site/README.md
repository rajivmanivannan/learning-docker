

# Provide permission to execute:
```
$ chmod +x wrapper.sh
```

# Build a docker image “static-site”
```
$ docker build -t static-site .
```

# To view images in the docker
```
$ docker images
```

# To tag a docker image
```
$ docker tag a3e4634f6d1d rajivmanivannan/static-site:latest
```

# To push the docker image to docker hub:
```
$ docker push rajivmanivannan/static-site
```

# To run the docker image in the available port:
```
$ docker run -d -P --name static-site rajivmanivannan/static-site:latest
```

# To see the port assigned to your image
```
$ docker port static-site
```

# To run the image with specified port:
```
$ docker run -p 8888:80 rajivmanivannan/static-site
```

# To see the result
```
http://localhost:8888
```

# To stop all docker container: 
```
$ docker stop $(docker ps -a -q)
```

# To remove all docker container:
```
$ docker rm $(docker ps -a -q)
```

# To remove docker image:
```
$ docker rmi rajivmanivannan/static-site:latest
```
