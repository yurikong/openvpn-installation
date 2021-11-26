# OpenVPN Installation Guide
###### on server [ubuntu 18.04/20.04]
	1. sudo apt update
	2. sudo apt upgrade
	3. sudo apt autoremove
	4. sudo apt clean
	5. sudo passwd root
		* [enter new password]
	6. su root
		* [enter password]
	7. passwd [user]
		* [enter new password]
	8. vi ~/../etc/ssh/sshd_config
		* LoginGraceTime 5m
		* PermitRootLogin yes
		* StrictModes no
		* PasswordAuthentication yes
	9. /etc/init.d/ssh restart
###### reboot server && ssh into server as root
	10. ssh root@[server-ip]
	11. wget https://git.io/vpn -O openvpn-install.sh
	12. bash openvpn-install.sh
		* DNS server -> Google
###### on local machine
	13. cd desktop
	14. scp root@[server-ip]:~/[client-name].ovpn .

# Note
### The purpose of root login is only for convenience.
###### For security purposes, use certificate to login, see modifications below
	7. not needed
	8. vi ~/../etc/ssh/sshd_config
		* PermitRootLogin no
		* StrictModes yes
		* PasswordAuthentication no
	10. ssh -i [path-to-certificate] [user]@[server-ip]
###### run step 6 again before proceeding to the rest!

Happy Tunneling! 😀
