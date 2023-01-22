# Docker-Containers
Container based virtualization technology using Docker

Docker commands : 


Appendix: Summary of Docker Commands
Commands Usage
docker –version to get the currently installed version of docker.
docker pull to pull images from the docker repository(hub.docker.com).
docker run -it -d to create a container from an image.
docker container ls / docker ps to list the running containers.
docker container ls -a / docker ps -a to show all the running and exited containers.
docker exec -it bash to access the running container.
docker container stop <hash> / docker stop
<hash>
Gracefully stops a running container
docker container kill <hash> Forces shutdown of the specified container
docker container rm <hash> Removes specified container from this machine
docker container rm $(docker container ls -a -q) Removes all containers
docker container rm -f $(docker container ls -a -q) Forcefully removes all containers
docker commit <username/imagename> creates a new image of an edited container on the local system.
docker push <username/image name> to push an image to the docker hub repository.
docker images / docker image ls lists all the locally stored docker images.
docker image rm $(docker image ls -a -q) Removes all Images
docker rm is used to delete a stopped container.
docker rmi <image id> / docker image rm <image
id>
Is used to delete an image from local storage.
docker build is used to build an image from a specified docker file.
docker build -t friendlyname . Is used to create image using this directory's Dockerfile
docker run -p 4000:80 friendlyname Run "friendlyname" mapping port 4000 to 80
docker run -d -p 4000:80 friendlyname Same thing, but in detached mode
docker login Log in CLI session using your Docker credential
docker tag <image> username/repository:tag Tag <image> for upload to registry
docker push username/repository:tag Upload tagged image to registry
docker run username/repository:tag Run image from a registry
