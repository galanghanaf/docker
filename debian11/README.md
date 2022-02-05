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
exit
```

## Running debian11 container
```
sudo docker exec -it debian11
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

## Get ip on debian11 container
```
apt install iproute2
```

## Get ssh on debian11 container
```
apt install openssh-server
```
```
apt install openssh-client
```
- Configuration SSH on debian 11 container
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
