# Configure Network Wireless With Tp link r8188eu 

Tanpa Network yang terhubung dengan komputer Installasi Arch linux
akan semakin menjadi rumit. Ada beberapa device yang akan langsung
bisa digunakan untuk Menjalankan iwd (iwctl). 

Untuk Device Tp link TL-WN725N saya tidak tau kenapa tidak bisa di deteksi dengan iwctl, 
Akan tetapi jika anda menggunakan nmcli device tersebut bisa di deteksi dan berjalan lancar.
Ada Beberapa tahapan saat saya melakukan instalasi arch linux. Di saat saya 
Melakukan Instalasi arch linux saya mengunakan Wireless Adapter 802.11N lalu setelah 
Instalasi selesai saya menggunakan TP Link TL-WN725N ( Mungkin Sebenarnya TP Link TL-WN725N 
Bisa digunakan jika modulenya sudah di load)

## Cara menghubungkan Wireless adapter 
```
lsmod | grep r8188eu # jika ada maka Load module tersebut 
modprobe r8188eu # Load module 
modprobe -r r8188eu # Ini hanya untuk unload module 
```
Jika Module tersebut tidak ada install dengan yay 
```
yay -S 8188eu-dkms
```
Agar Module tersebut selalu jalan saat komputer dihidupkan, Buat file 
```
vim /etc/modules-load.d/r8188eu.conf
r8188eu # hanya ini isinya

```
## Connect to Wireless ssid 

```
# untuk wifi
sudo pacman -S wpa_supplicant wireless_tools networkmanager
# mobile network
sudo pacman -S modemmanager mobile-broadband-provider-info usb_modeswitch
# For User Interface, after dowload run 'nmtui'
sudo pacman -S nm-connection-editor network-manager-applet
# Hidupkan network manager
sudo systemctl enable NetworkManager.service
# Matikan dhcpd agar tidak konflik
sudo systemctl disable dhcpcd.service
# jika butuh bantuan wireless aktivkan
sudo systemctl enable wpa_supplicant.service
# jalankan networkmanager
sudo systemctl start NetworkManager.service
# optional
sudo reboot
# cari wifi
nmcli device wifi list
# hubungkan ke jaringan
nmcli device wifi connect <SSID> password <SSID_password>
# list semua koneksi
nmcli connection show
# status device
nmcli --ask device wifi connect <ssid>
# Disconnect Interface
nmcli device disconnect <interface>
```
sumber <https://linuxhint.com/arch_linux_network_manager/> <br> <https://www.google.com/amp/s/www.makeuseof.com/connect-to-wifi-with-nmcli/amp/> <br> <https://itectec.com/unixlinux/linux-unable-to-connect-to-any-wifi-with-networkmanager-due-to-error-secrets-were-required-but-not-provided/> <br> <https://forum.salixos.org/viewtopic.php?f=30&t=7284>

~~~
<https://wiki.archlinux.org/title/Kernel_module> <br>
<https://unix.stackexchange.com/questions/71064/systemd-automate-modprobe-command-at-boot-time>


