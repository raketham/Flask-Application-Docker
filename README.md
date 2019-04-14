# Flask-Application-Docker
# Prerequisites:

Python 3.6
Flask
docker

# What Is Docker?

Docker is a tool which helps to create, deploy, and run applications by using containers. 

https://www.docker.com/get-started

Containers are a group of processes run in isolation, these processes are running in a shared kernel.

# Build the docker image

$ docker image build -t python-hello-world .

Docker List command 

$ docker image ls

# Run the docker container

$ docker run -p 8888:5000 -d python-hello-world

 # Access The application from the host machine
 
 avigate to http://localhost:8888 in a browser to see the results.
You should see "Hello World!" in your browser.


# Check the log output of the container

$ docker container ls

you can see the container is running

$ docker container logs container id

# Stop a docker container

$ docker container stop container id

# Remove the stopped containers

$ docker system prune
