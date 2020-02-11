# Roger_skyline_1
The purpose of this project is to proceed with the installation of a Virtual Machine, to discover the system and network bases as well as the many services used on a server machine.

#1 : Mettre a jour les paquets
sudo apt-get update

sudo apt-get upgrade

sudo apt-get install sudo

#2 : Creation d'un user & se connecter

sudo adduser [user]

ajout de l'utilisateur dans le fichier sudoers qui lui permettra d'utiliser la commande sudo

usermod -aG sudo [user]

su - [user]

#3 : Configuration Interfaces Reseaux
editer le fichier /etc/network/interfaces

modifier la derniere ligne de iface eth0 inet dhcp a iface eth0 inet static

modifier la partie #Primary network interfaces pour :

auto enp0s3
iface enp0s3 inet static
->	address 192.168.1.1
->	netmask 255.255.255.252
