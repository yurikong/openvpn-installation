# OpenVPN Installation Guide
steps to install openvpn server

## sudo apt update
## sudo apt upgrade
## sudo apt autoremove
## sudo apt clean
## sudo passwd root -> new password
## su root -> enter password
## cd ~/../etc/ssh
## vi sshd_config -> modify
	### LoginGraceTime 5m
	### PermitRootLogin yes
	### StrictModes no
	### PasswordAuthentication yes
## /etc/init.d/ssh restart
### reboot server && ssh into server as root
## wget https://git.io/vpn -O openvpn-install.sh
## bash openvpn-install.sh
### DNS server -> Google
### on my machine cmd
## cd desktop
## scp root@[server-ip]:~/[client-name].ovpn .
