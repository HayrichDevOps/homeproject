# homeproject
Prive projecten om mijn skills en kennis op te doen.


 Install Docker and Docker-Compose on Rocky Linux 8

# Step 1) Install updates and reboot 
 $ sudo dnf update -y
 Restart /reboot server

# Step 2) Configure Docker Package Repository & Install Docker
 $ sudo dnf config-manager --add-repo=https://download.docker.com/linux/centos/docker-ce.repo
 $ sudo dnf install -y docker-ce

## In case you are getting container.io error while installing docker-ce package then run following command.
$ sudo dnf install docker-ce --allowerasing -y

## STEP3) START AND ENABLE DOCKER SERVICE##
$ sudo systemctl start docker
$ sudo systemctl enable docker

## To verify the status of docker#
$ sudo systemctl status docker 

## If you wish local user to mange and run docker commands, then add the user to docker group using beneath command.#
$ sudo usermod -aG docker $USER

## CHECK DOCKER VERSION##
$ docker --version

## STEP 4) TEST DOCKER INSTALLATION##
$ docker run hello-world

## STEP 5) INSTALL DOCKER-COMPOSE##
$ dnf install -y curl
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose

## CHECK DOCKER-COMPOSE VERSION##
$ docker-compose --version

