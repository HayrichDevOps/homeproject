# homeproject
    Prive projecten om mijn skills en kennis op te doen.


    Install Docker and Docker-Compose on Rocky Linux 8 from the repository

 1.### Set up the repository.
    
    
    $ sudo yum install -y yum-utils
 
 
    $ sudo yum-config-manager \
       --add-repo \
       https://download.docker.com/linux/centos/docker-ce.repo
    

2.### Configure Docker Package Repository & Install Docker.
    
    
    $ sudo dnf config-manager --add-repo=https://download.docker.com/linux/centos/docker-ce.repo
    $ sudo dnf install -y docker-ce
    

3.### Install Docker Engine
    
    
    $ sudo yum install docker-ce docker-ce-cli containerd.io docker-compose-plugin
    
#####If prompted to accept the GPG key, verify that the fingerprint matches 060A 61C5 1B55 8A7F 742B 77AA C52F EB6B 621E 9F35, and if so, accept it.
##### This command installs Docker, but it doesn’t start Docker. It also creates a docker group, however, it doesn’t add any users to the group by default.

4.### To verify the status of docker.
    
    
    $ sudo systemctl status docker 
    

### If you wish local user to mange and run docker commands, then add the user to docker group using beneath command.
    
    $ sudo usermod -aG docker $USER
    

5.### Check docker version
    
    
    $ docker --version
    

6. ### Test docker installation
    
    $ docker run hello-world
    
    
7.### Install docker-compose.
    

    $ dnf install -y curl
    $ sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
    $ sudo chmod +x /usr/local/bin/docker-compose
    

8.### Check docker-compose version.
    

    $ docker-compose --version
    

