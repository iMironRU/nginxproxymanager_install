# nginxproxymanager_install

yum upgrade
yum install net-tools mc -y

# docker
sudo dnf install https://download.docker.com/linux/centos/7/x86_64/stable/Packages/containerd.io-1.2.10-3.2.el7.x86_64.rpm
yum install -y yum-utils device-mapper-persistent-data lvm2
sudo dnf install docker-ce -y
docker

# docker-compose
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version

systemctl start docker
sudo systemctl start docker

wget docker-compose.yml

docker-compose up -d

http://localhost:81/login

Email:    admin@example.com
Password: changeme

# link
https://help.reg.ru/hc/ru/articles/4408047645585-Как-установить-Docker-на-CentOS?
https://nginxproxymanager.com
