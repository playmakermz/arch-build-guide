# Install Desktop Manager

Setelah Membangun Operating System, Untuk Komputer yang di tujukan sebagai pemakaian sehari-hari 
akan Lebih muda jika memiliki Tampilan GUI ( Graphic User Interface ). 
Ada beberapa Aplikasi Yang akan lebih muda dijalankan Jika memiliki GUI sebagai Contoh
Editing video, Menggambar dan lain-lain. Untuk Komputer yang di tujukan Untuk Server
GUI itu tidak penting karena pada akhirnya komputer tersebut akan berjalan sendiri tanpa
harus ada orang yang melakukan perubahan System secara langsung.

Ada beberapa Desktop Manager yang Sudah saya coba dan jalankan.
Seperti Kde Plasma dan Gnome. Setelah Melakukan Instalasi Arch Saya sarankan untuk 
mendownload dan jalankan Desktop Manager karena itu akan sangat membantu dalam 
Penggunaan Sehari-hari. ( Ada Beberapa Saran Desktop Manager Yang belum saya buat dokumentasinya 
Seperti Awesome Desktop manager atau DWM, Saya Sarankan Anda Melihat dulu Desktop Manager seperti apa itu
Di youtube Atau platfrom lain)

## Install Kde Plasma
```
sudo pacman -Syu # Ingat Setelah Update biasakan untuk reboot
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
