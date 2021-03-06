## 网站长这样。
![coj](https://images2018.cnblogs.com/blog/1248976/201807/1248976-20180716164508752-1191793297.png)
![coj](https://images2018.cnblogs.com/blog/1248976/201807/1248976-20180725140408231-487641133.png)

# 须知
这个项目应该如何安装？

Collaborative Online Judge的安装方法总结：
# Install NodeJs:

sudo apt-get update

curl -sL https://deb.nodesource.com/setup_7.x | sudo -E bash -

sudo apt-get install -y nodejs

# Install Nodemon

sudo npm install -g nodemon

# Install git

sudo apt-get install git

# Install angular/cli

sudo npm install -g @angular/cli

# Install Redis

wget http://download.redis.io/releases/redis-3.2.6.tar.gz

tar xzf redis-3.2.6.tar.gz

cd redis-3.2.6

make

sudo make install

cd utils

sudo ./install_server.sh

# Install python 2.7: This is installed already in Ubuntu

# Install pip:

(sudo apt-get update)

sudo apt install python-pip

sudo pip install Flask

# Install Docker:

curl -fsSL https://get.docker.com/ | sh

Setup docker permission:

sudo usermod -aG docker $(whoami)

(you need to logout and login again after set permission)

To start docker when the system boots: sudo systemctl enable docker

# Install Nginx
(For ubuntu 16.04) Add following two lines into /etc/apt/sources.list

deb http://nginx.org/packages/ubuntu/ xenial nginx

deb-src http://nginx.org/packages/ubuntu/ xenial nginx

Then run:

sudo apt-get update

sudo apt-get install nginx

# FAQ

I failed to install newspaper package. It shows errors like 'could not build the egg.'

This is because an error when installing nltk dependency. Try following commands:

```
sudo apt-get install python-dev;

sudo apt-get install libxml2-dev libxslt-dev;

sudo apt-get install libjpeg-dev zlib1g-dev libpng12-dev;

sudo pip install --upgrade setuptools;

sudo pip install newspaper
```
# If above still not works, try here

1. Remove the repository version
```
sudo apt-get remove python-setup tools
```
2. if necessary, install pip again
```
wget https://bootstrap.pypa.io/get-pip.py;
sudo -H python get-pip.py
```
3. install setuptools via pip
```
sudo -H pip install -U pip setuptools
```
# still failed repeat from FAQ again
