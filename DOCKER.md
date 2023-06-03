# Docker Notes

## Fresh Setup

```sh
docker builder prune
```

## Docker

Running a single app in a docker instance (NodeJS)

Build the Docker image from your Dockerfile

```sh
docker build . -t emily/remix-app
# docker <action> <location of files> tag <custom tag name>
```

Create an instance of your Docker image within a container

```sh
docker run -p 3000:3000 -d emily/remix-app
# docker <action> <port tag> <map ports> <detached mode flag> <name of your container>
```

## Docker Compose

Create a `docker-compose.yaml` file

Run your docker container instance

```sh
docker-compose up --force-recreate --build --detach
```

Shut down and remove docker container instance

```sh
docker-compose down
```

## Upload to Docker Hub

Log into your Docker Hub via command line

```sh
docker login --username=<username>
docker login --email=<email>
# enter password
```

Tag your Docker image

```sh
docker tag <name-of-image/ID-of-image> <username/image-name:tag>
```

Push your Docker image

```sh
docker push <username/image-name:tag>
```
