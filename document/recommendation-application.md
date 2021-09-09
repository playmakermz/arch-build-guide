### Set Timezone
```
set timezone Asia/Jakarta
set timezone
```
#### Recommended package
```
pacman -S iwd net-tools netctl networkmanager devmon tlp bluez bluez-utils gparted lynx nitrogen pavucontrol ttf-dejavu ttf-inconsolata deluge  

pacman -S gutenprint usbview python-markdown gummi foliate nomacs firefox vlc qbittorrent unrar okular flameshot ark rhythmbox python-pip plasma-nm

sudo systemctl enable NetworkManager
```
#### Install yay
sumber <https://www.tecmint.com/install-yay-aur-helper-in-arch-linux-and-manjaro/>
```
pacman -S --needed git base-devel
pacman -S git
cd /opt
sudo git clone https://aur.archlinux.org/yay-git.git
sudo chown -R tecmint:tecmint ./yay-git
cd yay-git
makepkg -si
sudo yay -Syu 
yay -Syu --devel --timeupdate
```
#### Add display manager
```
pacman -S GDM # GDM adalah contoh
sudo systemctl enable gdm.service -f
```
#### Add other language firefox
sumber <https://unix.stackexchange.com/questions/356084/how-can-i-get-japanese-characters-to-show-properly-in-firefox-on-arch>
dan atur /etc/locale.gen locale-gen
```
sudo pacman -S noto-fonts-cjk noto-fonts-emoji noto-fonts
```
#### start openssh
```
sudo systemctl start sshd
systemctl status sshd
```
#### Atur pulseaudio
sumber <https://askubuntu.com/questions/879037/pavucontrol-stuck-at-establishing-connection-to-pulseaudio-please-wait>
``` pacman -S pulseaudio, reboot, pulseaudio --check, pulseaudio -D ```
#### Jalankan iwctl
```systemctl --now enable iwd, iwctl```
#### Atur brighness di amd laptop
```pacman -S brightnessctl, brightnessctl s 10```
#### Install neovim
```sudo pacman -S base-devel cmake unzip ninja tree-sitter curl, sudo pacman -S neovim```
spacevim <https://spacevim.org/quick-start-guide/#linux-and-macos>
#### Geekbench
```yay -S geekbench; geekbench```
#### Hubungkan dengan handphone
1. <https://www.youtube.com/watch?v=Ui__g9ThvCI&t=123s>
2. <https://wiki.archlinux.org/title/Media_Transfer_Protocol>
3. ```yay -S jmtpfs mtpfs ; sudo pacman -S kio-extras ; reboot``` Atau
+ ``` yay -S simple-mtpfs ; simple-mtpfs -l ;simple-mtpfs --device 1 ~/mnt```
#### Vlc
VLC automatically tries to use an available API, but you can override it by going to Tools > Preferences > Input & Codecs
<https://wiki.archlinux.org/title/VLC_media_player>

### screenshot
``` sudo pacman -S spectacle```
configure shortcut di kde

#### MP3 player
``` sudo pacman -S rhythmbox```
#### Install bluetooth
src <https://www.jeremymorgan.com/tutorials/linux/how-to-bluetooth-arch-linux/> |||
``` sudo pacman -S bluez bluez-utils blueman ``` |||
``` lsmod | grep btusb ; sudo vim /etc/bluetooth/main.conf ; sudo systemctl enable bluetooth.service ```AutoEnable=true
```sudo pacman -S pulseaudio pulseaudio-bluetooth```
```systemctl --user enable/start pulseaudio.service/socket```
<https://www.jeremymorgan.com/tutorials/linux/how-to-bluetooth-arch-linux/>
<https://bbs.archlinux.org/viewtopic.php?id=201496>

#### Disable kde wallet
<https://bbs.archlinux.org/viewtopic.php?id=202174>

#### Refrensi
+ <https://askubuntu.com/questions/707665/no-archiving-compressing-tool-in-dolphin-context-menu-kubuntu-15-10>
+ <https://help.ubuntu.com/community/NetworkManager>
