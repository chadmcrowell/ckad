# `docker` commands in week1

```bash
# run a docker container using the ubuntu image
docker run ubuntu

# list the running containers
docker ps

# list all containers (stopped or started)
docker ps -a

# run a docker container passing in a command entrypoint
docker run ubuntu sleep 5

# build a docker image from Dockerfile (in the current directory) and tag it 'ubuntu-sleeper'
docker build -t ubuntu-sleeper .

# run a container based on the image you just built (ubuntu-sleeper)
docker run ubuntu-sleeper

# run a container from the 'ubuntu-sleeper' image and tell it to sleep for 10 seconds at startup
docker run ubuntu-sleeper sleep 10

# from an entrypoint instruction in Dockerfile, run a container from the 'ubuntu-sleeper' image and tell it to sleep for 10 seconds at startup
docker run ubuntu-sleeper 10

# override the entrypoint with the docker run command
docker run --entrypoint sleep2.0 ubuntu-sleeper 10

# build an image from a file named 'Dockerfile' and tag it 'chadmcrowell/my-custom-app' 
docker build Dockerfile -t chadmcrowell/my-custom-app

# push the image you just built to the DockerHub image registry using the tag 'chadmcrowell/my-custom-app'
docker push chadmcrowell/my-custom-app


```