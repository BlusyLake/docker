Primeiras dependencias para começar a utilzar o sistema docker 

 sudo apt-get install docker docker.io docker-buildx docker-compose-v2
 sudo groupadd docker
 sudo usermod -aG docker $USER
 docker volume create portainer_data
 docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
