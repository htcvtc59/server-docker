
# DOCKER RUN : https://hub.docker.com/r/htcvtc59/linux 

### Debian

- `latest` -> `debian:latest`

### Generate ssh :
    
    ssh-keygen -q -N "" -t rsa
  
**RUN CONTAINER** :

    docker run -d -p 2222:22 -e AUTHORIZED_KEYS="`cat ~/.ssh/id_rsa.pub`" htcvtc59/linux

To connect to this container as root:

    ssh -p 2222 root@localhost
