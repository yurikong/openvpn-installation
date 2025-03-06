# OpenVPN Installation Guide

[![Security Status](https://www.murphysec.com/platform3/v3/badge/1618272099483811840.svg?t=1)](https://www.murphysec.com/accept?code=9c6666ec7566192047671c4b45ca7bde&type=1&from=2&t=2)

###### on server [ubuntu 18.04 / 20.04]
	1. sudo apt update
	2. sudo apt upgrade
	3. sudo apt autoremove
	4. sudo apt clean
	5. sudo passwd root
		* [enter new password]
	6. su root
		* [enter password]
###### reboot server && ssh into server as root
	7. ssh -i id_rsa.pem ubuntu@[server-ip]
	8. wget https://git.io/vpn -O openvpn-install.sh
	9. bash openvpn-install.sh
		* DNS server -> Google
  	10. cp [profile_name].ovpn /home/ubuntu/
###### on local machine
	11. cd desktop
	12. scp -i id_rsa.pem root@[server-ip]:~/[profile_name].ovpn .

Happy Tunneling! 😀
