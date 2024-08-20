COMANDOS LINUX

DEBIAN 12

RESPOSITORIOS DEBIAN 12
nano /etc/apt/sources.list

deb http://deb.debian.org/debian bookworm main non-free-firmware
deb-src http://deb.debian.org/debian bookworm main non-free-firmware

deb http://deb.debian.org/debian-security/ bookworm-security main non-free-firmware
deb-src http://deb.debian.org/debian-security/ bookworm-security main non-free-firmware

deb http://deb.debian.org/debian bookworm-updates main non-free-firmware
deb-src http://deb.debian.org/debian bookworm-updates main non-free-firmware


IP STATIC
nano /etc/network/interfaces

# This file describes the network interfaces available on your system
# and how to activate them. For more information, see interfaces(5).

source /etc/network/interfaces.d/*

# The loopback network interface
auto lo
iface lo inet loopback

auto ens18
iface ens18 inet static
        address 192.168.1.150
        netmask 255.255.255.0
        gateway 192.168.1.199
        dns-nameservers 192.168.1.199 8.8.8.8


HABILITAR SSH ROOT
nano /etc/ssh/sshd_config

alterar a linha "PermitRootLogin without-password" para "PermitRootLogin yes"
depois rodar o comando 
service ssh restart

TROCAR SENHA ROOT
passwd root
