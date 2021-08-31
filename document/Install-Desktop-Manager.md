# Install Desktop Manager

after installing Operating system i sugest try installing Desktop Manager it's will give a big help to 
user for their daily usage. in this section i only sugest two desktop manager because there is a ton 
desktop manager is open and worth it to use.

if you prefer tiling window manager:
- awesome <https://awesomewm.org/>
- qtile <http://www.qtile.org/>

## Install Kde Plasma
```
sudo pacman -Syu # optional rebot the device after update system 
sudo pacman -S xorg plasma plasma-wayland-session kde-applications
sudo systemctl enable sddm.service
reboot
```
About Kde <https://kde.org/>

##
```
sudo pacman -Syu
sudo pacman -S xorg xorg-server
sudo pacman -S gnome
sudo systemctl start gdm.service
sudo systemctl enable gdm.service
sudo pacman -S gnome-tweaks
reboot
```
About Gnome  <https://www.gnome.org/>
