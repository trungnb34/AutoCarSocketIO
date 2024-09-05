# AutoCarSocketIO 

#### install docker and docker-compose 

sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
apt-cache policy docker-ce
sudo apt install docker-ce
sudo systemctl status docker
sudo usermod -aG docker ${USER}
su - ${USER}
groups
sudo usermod -aG docker username
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose

#### Change file config on docker-compose.yml
in the field SERVER_RTMP. You must change the IP address to the server’s IP address. After that, you run this command 

#### Start server

docker-compose up -d

#### After that we have two server 
    1 : Server socket io with URL : http://{IP}:5000
    2 : Server stream width URL : rtmp://{IP}:1935
two servers will call from the client controller on jetson and GUI 