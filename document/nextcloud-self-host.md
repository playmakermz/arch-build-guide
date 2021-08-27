# Installation Nextcloud client-server software

Before we install nextcloud it's better using virtual machine ( exp virtualbox ),
The goal is build hosting service for your desktop.

## Install virtualbox Arch linux
src <https://wiki.archlinux.org/title/VirtualBox> dan <https://wiki.archlinux.org/title/VirtualBox/Install_Arch_Linux_as_a_guest>
```
sudo pacman -S virtualbox
# akan ada 2 pilihan, untuk linux versi terbaru pilih nomor 2, untuk linux versi lain pilih nomor 1
sudo modprobe vboxdrv
sudo pacman -Syu virtualbox-guest-utils
```

#### Install self hosting

1. Gunakan ubuntu server ( oracle virtual box )
2. sudo snap install nextcloud
3. sudo nextcloud.manual-install username-anda password-anda
4. sudo nextcloud.occ config:system:set trusted_domains 1 --value=example.com # untuk domain gunakan ip contoh 192.168.100.10
5. sudo nextcloud.occ config:system:get trusted_domains
6. sudo nextcloud.enable-https self-signed
7. sudo ufw allow 80,443/tcp



Judul  |   Link                       | Deskripsi
------ | ---------------------------- | ----------
sandstrom | <https://sandstorm.io/install> | Sandstrom self hosting
Install nextcloud | <https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-nextcloud-on-ubuntu-20-04> | cara install nextcloud
Snap | <https://snapcraft.io/docs/installing-snap-on-arch-linux> | install snap arch
