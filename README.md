## How to install docker 

check this tutorial

[How To Install and Use Docker on Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04)

## How to fix docker: Got permission denied while trying to connect to the Docker daemon socket
According to the official Docker docs here:

https://docs.docker.com/install/linux/linux-postinstall/#manage-docker-as-a-non-root-user

You need to do the following:

To create the docker group and add your user.  Create the docker group, need to loog out and log back in so that your group membership is re-evaluated or type the following command
```bash
  sudo groupadd docker
  sudo usermod -aG docker ${USER}
  su -s ${USER}
```

getting problem that after restarting the ubuntu server docker was loosing the access if I have given the permission via
```bash
  sudo chmod 666 /var/run/docker.sock  
```


