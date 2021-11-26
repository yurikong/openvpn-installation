# OpenVPN Installation Guide
###### on server
	sudo apt update
	sudo apt upgrade
	sudo apt autoremove
	sudo apt clean
	sudo passwd root -> new password
	su root -> enter password
	passwd [user] -> new password
	cd ~/../etc/ssh
	vi sshd_config -> modify
		LoginGraceTime 5m
		PermitRootLogin yes
		StrictModes no
		PasswordAuthentication yes
	/etc/init.d/ssh restart
###### reboot server && ssh into server as root
	wget https://git.io/vpn -O openvpn-install.sh
	bash openvpn-install.sh
		DNS server -> Google
###### on local machine
	cd desktop
	scp root@[server-ip]:~/[client-name].ovpn .
