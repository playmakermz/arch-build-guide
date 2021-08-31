# Configure Network Wireless With Tp link r8188eu 

Without Network connected to computer it's hard to install arch linux .
there are several devices that will immediately in use when user start arch linux 
for more info <https://wiki.archlinux.org/title/Network_configuration>.

for user using wireless network, i recommended using iwctl, nmtui or nmcli.

for device Tp link TL-WN725N i don't know why this device is can't be detected with iwd ( iwctl ),
for installing arch linux i using Wireless adapter 802.11N, 
if user ecounter a problem i suggest try load the device module and connect to internet
using NetworkManager.

## Load Wireless device module
try using lsub to search your device name ( for me is 'Bus 003 Device 006: ID 0bda:8179 Realtek Semiconductor Corp. RTL8188EUS 802.11n Wireless Network Adapter')
'lsusb'
```
lsmod | grep r8188eu # change r8188eu to your device name, for me even only 8188 is fine
modprobe r8188eu # Load a module 
```
`modprobe -r r8188eu # to unload module `

if module is not found try installing module with yay or other aur helper
```
yay -S 8188eu-dkms
```
To make module is autoload when computer start running, create new file
```
vim /etc/modules-load.d/r8188eu.conf
r8188eu # hanya ini isinya
```

## Connect to Wireless ssid 

for me i only install wifi section is more than enough
```
# Wifi network section  
sudo pacman -S wpa_supplicant wireless_tools networkmanager
# mobile network
sudo pacman -S modemmanager mobile-broadband-provider-info usb_modeswitch

# For User Interface, after dowload run 'nmtui'
sudo pacman -S nm-connection-editor network-manager-applet
# Enable NetworkManager 
sudo systemctl enable NetworkManager.service
# enable wpa_supplicant 
sudo systemctl enable wpa_supplicant.service
# start networkmanager
sudo systemctl start NetworkManager.service
# optional
sudo reboot

# search wifi ssid
nmcli device wifi list
# connect to wireless ssid
nmcli device wifi connect <SSID> password <SSID_password>
# list all connection
nmcli connection show
# status device
nmcli --ask device wifi connect <ssid>
# Disconnect Interface
nmcli device disconnect <interface>
```
source <https://linuxhint.com/arch_linux_network_manager/> <br> <https://www.google.com/amp/s/www.makeuseof.com/connect-to-wifi-with-nmcli/amp/> <br> <https://itectec.com/unixlinux/linux-unable-to-connect-to-any-wifi-with-networkmanager-due-to-error-secrets-were-required-but-not-provided/> <br> <https://forum.salixos.org/viewtopic.php?f=30&t=7284>

~~~
<https://wiki.archlinux.org/title/Kernel_module> <br>
<https://unix.stackexchange.com/questions/71064/systemd-automate-modprobe-command-at-boot-time>


