In this task, you will containerize an application that is already written for you. Do the following steps:
1. Clone the project’s repository from Github.
student@6312vm-csr00$ git clone -b v1 https://github.com/inwk6312course/dockerapp.git
student@6312vm-csr00$ cd dockerapp
student@6312vm-csr00$ ls

2. Build the Image from the Dockerfile found in the repository. Review the contents of the Dockerfile
before building. The -t flag is used to tag the image to a custom name of our choice. We can also tag
an image, think of it as putting a version on the image. In this case we tag the image v1
student@6312vm-csr00$ docker build -t dockerapp:v1 .

3. Copy the Image id of the newly built image by running
student@6312vm-csr00$ docker image ls

4. Run the image as a container. The -d flag run the container in detached mode.
student@6312vm-csr00$ docker run -d -p 5000:5000 <<image-id>>
  
5. Visit the homepage of the application with the Curl program
student@6312vm-csr00$ curl localhost:5000
  
  
  ![image](https://user-images.githubusercontent.com/35003840/213943532-80ebcbc6-9c74-4714-92c3-de0983173e82.png)
