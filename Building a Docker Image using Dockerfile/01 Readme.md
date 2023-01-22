Next, we will learn how to build our own Ubuntu Docker image instead of using the one from Docker Hub.
1. Download the Ubuntu Dockerfile and its dependencies.
student@6312vm-csr00$ `git clone --single-branch --branch dist-amd64
https://github.com/tianon/docker-brew-ubuntu-core.git`

2. Change directory to the cloned repository and ensure that the Dockerfile is present.
student@6312vm-csr00$ `cd docker-brew-ubuntu-core/xenial`
student@6312vm-csr00$ `ls .`

3. Build a new image using Docker and the Dockerfile.
student@6312vm-csr00$ `docker image build .`
Docker prints progress messages as it builds the Ubuntu image. Once it finishes building the image, Docker
assigns it a randomly chosen name.

4. Run the command:
student@6312vm-csr00$ `docker images ls`
Docker lists all the images on your system, including both the newly built one and any that you previously
downloaded. You can tell which image is the one you just created by examining the list; it's the only image
that isn't associated with a repository.

5. Run the newly created Docker image by giving the randomly-chosen ID to Docker:
student@6312vm-csr00$ `docker run -ti <your image ID>`
The newly-created image behaves exactly the same way as the Ubuntu image from Docker Hub, because
it is built from the same Dockerfile. You now have a bash root prompt.

### Push the image to Docker Hub : https://jsta.github.io/r-docker-tutorial/04-Dockerhub.html

Step 1 : Make sure the server is already connected to Docker Hub :  `docker login -u docker_hub_user_name `

Step 2 : Name/Tag the image : `docker tag image_id your_docker_image`

Step 3: connect with docker hub image : `docker your_docker_image docker_hub_user_name/docker_hub_image`

Step 4: Push the image to Docker Hub : `docker push docker_hub_user_name/docker_hub_image`

Output : 

![image](https://user-images.githubusercontent.com/35003840/213896626-e238a65d-4d74-444a-8f70-d25634d3f8e2.png)

Uploaded to Docker Hub : 

![image](https://user-images.githubusercontent.com/35003840/213896643-9a8848f1-bde5-4fae-8f5f-fee2f91c253b.png)


