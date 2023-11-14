# Docker Cheatsheet

## Basic Docker Commands

| Command | Explanation | Example |
|---------|-------------|---------|
| `docker pull` | Pulls an image from Docker Hub | `docker pull nginx` |
| `docker run` | Runs a container from an image | `docker run -d -p 80:80 nginx` |
| `docker ps` | Lists all running containers | `docker ps` |
| `docker stop` | Stops a running container | `docker stop <container_id>` |
| `docker rm` | Removes a stopped container | `docker rm <container_id>` |
| `docker exec` | Runs a command in a running container | `docker exec -it <container_id> bash` |
| `docker logs` | Displays the logs of a container | `docker logs <container_id>` |

## Docker Images

| Concept | Explanation | Example |
|---------|-------------|---------|
| Dockerfile | A text file with build instructions | `FROM ubuntu:latest` |
| Base image | The image a Dockerfile is based on | `ubuntu:latest` |
| Layers | Efficient image building with layers | `FROM ubuntu:latest`<br>`COPY index.html /usr/share/nginx/html`<br>`EXPOSE 80` |
| `docker build` | Builds an image from a Dockerfile | `docker build -t my-image:tag .` |
| `docker images` | Lists all local images | `docker images` |

## Docker Networking

| Concept | Explanation | Example |
|---------|-------------|---------|
| Docker network | Virtual network for container communication | `docker network create my-network` |
| Port mapping | Maps container port to host machine port | `docker run -d -p 80:80 nginx` |
| Link | Links two containers for communication by name | `docker run -d --link my-database:db mysql` |
| `docker network ls` | Lists all Docker networks | `docker network ls` |

## Docker Volumes

| Concept | Explanation | Example |
|---------|-------------|---------|
| Docker volume | Persistent storage for containers | `docker volume create my-volume` |
| Volume mount | Mounts a volume to a container directory | `docker run -d -v my-volume:/var/lib/mysql mysql` |
| `docker volume ls` | Lists all Docker volumes | `docker volume ls` |
| `docker inspect` | Displays detailed information about a container | `docker inspect <container_id>` |

