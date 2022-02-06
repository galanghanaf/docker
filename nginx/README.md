# Nginx on Docker

## Pulling Image
```
docker pull nginx:latest
```

## Running Nginx Image
```
docker run -d --name nginx -p 8080:80 nginx:latest 
```

## Configure Nginx Container
```
docker exec -it nginx /bin/bash
```
