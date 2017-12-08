# messypi

## installation notes:

### Pi setup

Set hostname
```
sudo echo "ppnyserver" > /etc/hostname
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install avahi-daemon
```
Enable SSH

`sudo raspi-config`
Interfacing Options > SSH 

Set DNS servers
```
sudo echo "interface eth0
static domain_name_servers=8.8.8.8" >> /etc/dhcpcd.conf
```

### MessyPi installation

`git clone https://github.com/PrimeProduce/messypi.git /home/pi/messypi`
