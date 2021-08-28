# Cek BIOS atau UEFI
```
ls /sys/firmware/efi #or
sudo efibootmgr 
```
## Format disk
minimal format ( 50MB BIOS BOOT, 512MB boot, 9GB root )
```
fdisk -l # cek disk
cfdisk -z # hapus semua partisi dan opsi GPT
cfdisk /dev/sda # buat partisi 
# dalam cfdisk partisi satu buat menjadi BIOS boot
# partisi dua ext2
# partisi tiga root
mkfs.ext2 /dev/sda2 # boot
mkfs.ext4 /dev/sda3 # root
```
# Configure Mirror for download package ( It' not recommended )
```
pacman -Syy
pacman -S reflector
cp /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.bak
reflector -c "IN" -f 12 -l 10 -n 12 --save /etc/pacman.d/mirrorlist
```
# Base Install
```
mount /dev/sda3 /mnt
pacstrap /mnt base linux linux-firmware
genfstab -U /mnt >> /mnt/etc/fstab    
```
# Chroot
```
arch-chroot /mnt
ln -sf /usr/share/zoneinfo/Asia/Jakarta /etc/localtime
hwclock --systohc
pacman -S vim
vim /etc/locale.gen
locale-gen
echo lieat > /etc/hostname
# vim /etc/hosts
127.0.0.1       localhost
::1             localhost
127.0.1.1       localhost
```
# set users and password
```
passwd
useradd -m example
passwd example
usermod -aG wheel,audio,video,optical,storage example
```
# sudo :
```
pacman -S sudo
EDITOR=vim visudo
# cari wheel ALL=(ALL) ALL
```
# GRUB For UEFI
```
pacman -S grub
pacman -S efibootmgr dosfstools os-prober mtools
mkdir /boot/EFI
mount /dev/sda1 /boot/EFI
grub-install --target=x86_64-efi  --bootloader-id=grub_uefi --recheck
grub-mkconfig -o /boot/grub/grub.cfg
```
# GRUB For MBR ( Recomended for easy install)
```
pacman -S grub efibootmgr dosfstools os-prober mtools && mkdir /boot/efi && mount /dev/sda2 /boot/efi 
grub-install --target=i386-pc /dev/sda
grub-mkconfig -o /boot/grub/grub.cfg
```
# Networking
```
pacman -S networkmanager
systemctl enable NetworkManager
```
# Install VGA amd 
```
sudo pacman -S xorg xorg-xinit
sudo pacman -S xterm xorg-tw 
sudo pacman -S mesa xf86-video-amdgpu xf86-video-ati libva-mesa-driver vulkan-radeon 
```
src <https://github.com/archlinux/archinstall/blob/master/archinstall/lib/hardware.py>
# reboot
```
exit # exit chroot
reboot 
```
***
### Refrensi
<https://youtu.be/PQgyW10xD8s> <https://itsfoss.com/install-kde-arch-linux/> <br>
<https://phoenixnap.com/kb/arch-linux-gnome> install gnome <br>
<https://wiki.archlinux.org/title/Installation_guide>
