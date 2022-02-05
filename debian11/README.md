# Debian 11 on Docker

## Pulling Image
```
sudo docker pull debian:11
```

## Running Debian Image
```
sudo docker run -it --name debian11 debian:11 /bin/bash
```

## Exit from debian11 cotainer
```
root@f5724af38j7p:/# exit
```

## Start debian11 container
```
sudo docker start debian11
```

## Check debian11 container running or not
```
sudo docker ps
```

## Running debian11 container
```
sudo docker exec -it debian11 /bin/bash
```

## Get Update debian11 container
```
apt update
```

## Get root password on debian11 container
```
passwd root
```

## Get vim on debian11 container
```
apt install vim
```

## Get ssh on debian11 container
```
apt install openssh-server
```
```
apt install openssh-client
```
- SSH configuration on debian 11 container
```
vim /etc/ssh/sshd_config
```
```
PermitRootLogin without-password
change to
PermitRootLogin yes
```
```
and restart ssh
service ssh restart
```

## Get ip on debian11 container
```
apt install iproute2
```
- Exit from debian 11 container
```
root@f5724af38j7p:/# exit
```
- and get ip on debian11 container
```
docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' debian11
```
## Done
