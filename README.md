# Flask-Application-Docker
# Prerequisites:

Python 3.6
Flask
docker

# What Is Docker?

Docker is a tool which helps to create, deploy, and run applications by using containers. Docker provides developers and operators with a friendly interface to build, ship, and run containers on any environment. To install docker follow the link https://www.docker.com/get-started

Containers are a group of processes run in isolation, these processes are running in a shared kernel.

# Build the docker image

Run the following command to create the docker image from src directory, Pass in the -t parameter to name your image python-hello-world.
$ docker image build -t python-hello-world .
erify that your image shows in your image list:
$ docker image ls

# Run the docker container

$ docker run -p 5001:5000 -d python-hello-world

 # Access The application from the host machine
 
 avigate to http://localhost:5001 in a browser to see the results.
You should see "Hello World!" in your browser.


# Check the log output of the container

$ docker container ls
You should see your container id by running this command.


$ docker container logs [container id]
output should be look like : 
* Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
172.17.0.1 - - [28/Jun/2017 19:35:33] "GET / HTTP/1.1" 200 -

# Stop a docker container

$ docker container stop [container id]
Tip: You need to enter only enough digits of the ID to be unique. Three digits is typically adequate.

# Remove the stopped containers

$ docker system prune
