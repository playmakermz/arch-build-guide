# Ranger FIle manager

open file manager from terminal. The goal is to open file manager
and view image 

#### Ranger and file icon
```
git clone https://github.com/alexanderjeurissen/ranger_devicons ~/.config/ranger/plugins/ranger_devicons
echo "default_linemode devicons" >> $HOME/.config/ranger/rc.conf # sesuaikan dengan tempat rc.conf milik ranger
```
src <https://github.com/alexanderjeurissen/ranger_devicons>
#### Ranger Image view
```
sudo pacman -S uberzug
vim ~/.config/ranger/rc.conf
# isi di dalam
set preview_images true
set preview_images_method ueberzug
```
src: <https://github.com/ranger/ranger/wiki/Image-Previews> <https://askubuntu.com/questions/1222930/image-preview-doesnt-work-in-ranger>
