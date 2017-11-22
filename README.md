# messypi

## installation notes:

install messypi

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
sudo echo "nameserver 8.8.8.8" > /etc/resolv.conf
sudo echo "nameserver 8.8.4.4" >> /etc/resolv.conf
```
