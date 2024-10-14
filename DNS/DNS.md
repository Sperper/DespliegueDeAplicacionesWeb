# DNS
## Comando para poner una IP fija:
- sudo nano /etc/network/interfaces
- sudo systemctl restart networking
- sudo /etc/init.d/networking restart
- ip addr show eth0

## Fichero named.conf.options
- sudo nano /etc/bind/named.conf.options
- sudo systemctl status bind9

## Fichero resolv.conf
- sudo nano /etc/resolv.conf