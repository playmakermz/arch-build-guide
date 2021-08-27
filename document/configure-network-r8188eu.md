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
************
******~~~
<https://wiki.archlinux.org/title/Kernel_module> <br>
<https://unix.stackexchange.com/questions/71064/systemd-automate-modprobe-command-at-boot-time>
