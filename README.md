# messypi

## Pi setup

#### Change password
`passwd`

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

select: `Interfacing Options > SSH`, turn SSH on.

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

## Polyglot installation

Follow https://ud-polyglot.readthedocs.io/en/development/usage.html#installation


## MessyPi installation
```
mkdir ~/github
git clone https://github.com/PrimeProduce/messypi.git /home/pi/github/messypi
```

## Process management with pm2

#### Install pm2
`npm install pm2@latest -g`

#### Setup pm2 startup script
Run `pm2 startup`, then run the resulting command

#### Run scripts with pm2 (for example, messybot)
`pm2 start app/messybot.js`

#### Save scripts for startup 
`pm2 save`


