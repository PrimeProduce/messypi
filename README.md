# messypi

## Pi setup

#### Set hostname
```
sudo echo "ppnyserver" > /etc/hostname
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install avahi-daemon
```
Edit `/etc/hosts` so there is a line:
`127.0.0.1       localhost localhost.localdomain ppnyserver`

#### Enable SSH

`sudo raspi-config`
Interfacing Options > SSH 

#### Set DNS servers
```
sudo echo "interface eth0
static domain_name_servers=8.8.8.8" >> /etc/dhcpcd.conf
```

#### Install/update Node
```
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs
```

#### Install Vim

`sudo apt-get install vim`

## MessyPi installation

`git clone https://github.com/PrimeProduce/messypi.git /home/pi/messypi`
