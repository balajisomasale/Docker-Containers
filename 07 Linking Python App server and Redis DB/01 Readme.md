## Task 7: Linking Two Containers

1. Start up a Redis container.
student@6312vm-csr00$ docker run -d --name redis redis:3.2.0

2. Clone the Python web application.
If you are already working from the cloned Git repository from the previous task, then you can use
the checkout command to change to a different branch (v2) which contains the updated code and
move to the next step.

student@6312vm-csr00$ git checkout v2

Else If you are starting from a fresh older, then you should use the clone command to download the
v2 branch and move to the next step

student@6312vm-csr00$ git clone -b v2 https://github.com/inwk6312course/dockerapp.git


3. Build the Python web application
student@6312vm-csr00$ `docker build -t dockerapp:v2 .`

4. Run the web application and link with the Redis container
5. 
student@6312vm-csr00$ `docker run -d -p 5000:5000 --link redis dockerapp:v2`

5. Connect to the web application and inspect the hosts file to see how Docker registers the hostname
of the running redis container with an IP address. This is how the web application is able to connect
with the redis container using an IP address or the hostname

student@6312vm-csr00$ `docker exec -it <<dockerApp-containerId>> bash`
  
admin@4f734e68b935:/app$ more /etc/hosts
  
6. Ping the redis container to confirm connectivity
`admin@4f734e68b935$ ping redis`
