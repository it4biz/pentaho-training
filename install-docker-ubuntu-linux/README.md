# Install Docker and Docker Compose on Ubuntu Linux Server

# Install git
sudo apt-get install git


# Install R
sudo apt-get install r-base
sudo apt-get install littler


sudo apt-get update
sudo apt-get install r-base r-base-dev

#The best way to install packages is to use the up-to-date packages from RutteR PPA. 

#Install the PPA using:
sudo add-apt-repository ppa:marutter/rrutter
sudo apt-get update

#and packages can simply be installed using
sudo apt-get install r-cran-reshape2
sudo apt-get install r-cran-ggplot2
sudo apt-get install r-cran-reshape2
sudo apt-get install r-cran-rjava

#Install Docker
# https://docs.docker.com/installation/ubuntulinux/

uname -r

apt-key adv --keyserver hkp://pgp.mit.edu:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D

sudo vi /etc/apt/sources.list.d/docker.list

# Ubuntu Trusty
deb https://apt.dockerproject.org/repo ubuntu-trusty main

apt-get update

apt-get purge lxc-docker*

apt-cache policy docker-engine

sudo apt-get update

sudo apt-get install linux-image-generic-lts-trusty

sudo reboot

sudo apt-get update

sudo apt-get install docker-engine

sudo docker run hello-world

# Install Docker Compose
sudo curl -L https://github.com/docker/compose/releases/download/1.4.2/docker-compose-`uname -s`-`uname -m` > sudo /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

#Get Pip Install
wget https://bootstrap.pypa.io/get-pip.py

#Install Pip Install
sudo python get-pip.py

sudo pip install -U docker-compose==1.4.2

# Test Docker Compose
docker-compose --version




