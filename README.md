
# DOCKER RUN : https://hub.docker.com/r/htcvtc59/ubuntu-server/

### Debian

- `latest` -> `debian:latest`

### Generate ssh :
    
    ssh-keygen -q -N "" -t rsa
  
**RUN CONTAINER** :

    docker run -d -p 2222:22 -e AUTHORIZED_KEYS="`cat ~/.ssh/id_rsa.pub`" htcvtc59/ubuntu-server

To connect to this container as root:

    ssh -p 2222 root@localhost