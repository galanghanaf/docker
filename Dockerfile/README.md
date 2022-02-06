# Dockerfile

## Create Dockerfile

```
touch Dockerfile
```

## Enter to Dockerfile

```
vim Dockerfile
```

## Add this command to Dockerfile

```
FROM ubuntu:20.04
LABEL maintainer="Galang Hanafi <galanghanafi8@gmail.com>"
RUN apt update && apt upgrade -y
RUN apt install vim nginx iproute2 -y
CMD ["/bin/bash"]
```

## Build Dockerfile

```
sudo docker build -t ubuntults:0.1 .
```

- after that the dockerfile becomes a docker image

## Test Docker Image

```
sudo docker run -d --name ubuntults ubuntults:20.04
```

## Running nginx

```
sudo docker exec -it ubuntults /bin/bash -c "service nginx start"
```

## After that, get the container ip with command

```
sudo docker exec -it ubuntults /bin/bash -c "ip addr"
```
