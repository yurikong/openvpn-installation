# OpenVPN Installation Guide

[![Security Status](https://www.murphysec.com/platform3/v3/badge/1618272099483811840.svg?t=1)](https://www.murphysec.com/accept?code=9c6666ec7566192047671c4b45ca7bde&type=1&from=2&t=2)

###### on server [ubuntu 18.04 / 20.04]
	1. sudo apt update
	2. sudo apt upgrade
	3. sudo apt autoremove
	4. sudo apt clean
	5. sudo passwd root
		- [enter new password]
	6. su root
		- [enter password]
###### modify ssh settings
	7. vi /etc/ssh/sshd_config
		- PermitRootLogin yes
		- PasswordAuthentication yes
	8. sudo systemctl restart ssh
###### reboot server && ssh into server as root
	9. ssh -i id_rsa.pem ubuntu@[server-ip]
	10. wget https://git.io/vpn -O openvpn-install.sh
	11. bash openvpn-install.sh
		- DNS server -> Google
  	12. cp [profile_name].ovpn /home/ubuntu/
###### on local machine
	13. cd desktop
	14. scp -i id_rsa.pem root@[server-ip]:~/[profile_name].ovpn .
 	15. scp -i id_rsa.pem ubuntu@[server-ip]:~/[profile_name].ovpn . // if root doesn't work, try this!

Happy Tunneling! 😀
