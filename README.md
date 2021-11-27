# docker setup
#Prerequisites
#Check Linux Kernel
uname -r
Result: 5.8.0-43-generic

#update kernel
sudo apt-get update

#Install docker as per website instruction

#check docker installed
sudo docker run hello-world


#add sudo user group
sudo usermod -aG docker narayan

#run hello-world without sudo
docker run hello-world

#if you find any error, refer the help given below.

Example 1: Got permission denied while trying to connect to the Docker daemon socket

sudo chmod 666 /var/run/docker.sock

Example 2: Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get http://%2Fvar%2Frun%2Fdocker.sock/v1.40/containers/json: dial unix /var/run/docker.sock: connect: permission denied

sudo usermod -aG docker ${USER}

Example 3: Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock

sudo chmod 666 /var/run/docker.sock

Example 4: Server: ERROR: Got permission denied while trying to connect to the Docker daemon socket

sudo newgroup docker
sudo chmod 666 /var/run/docker.sock
sudo usermod -aG docker ${USER}

Example 5: Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock:

newgrp docker

Example 6: Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Post http://%2Fvar%2Frun%2Fdocker.sock/v1.24/auth: dial unix /var/run/docker.sock: connect: permission denied

docker permission for linux ec2
