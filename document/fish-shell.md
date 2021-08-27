## Install And configure Fish Shell

Using fish shell to make Terminal more beautiful

```
curl -L https://get.oh-my.fish > install
fish install --path=~/.local/share/omf --config=~/.config/omf
# lakukan configure terminal agar fish bisa paten
```
## Install theme and use theme
```
omf install bobthefish
omf theme bobthefish
omf list
```
## select theme for bobthefish
```
set -g theme_nerd_fonts yes
set theme_color_scheme nord  
## untuk membuat ini selalu jalan / default
vim ~/.config/fish/config.fish  
## isi dari config.fish
if status is-interactive
# Commands to run in interactive sessions can go here
set theme_color_scheme nord
end

```
## Delete theme
```
omf remove themename
```
## install find launcher
```
yay -S ulauncher
# kata kunci ctrl + space
```
#### refrensi 
<https://github.com/oh-my-fish/oh-my-fish> <br> <https://github.com/oh-my-fish/oh-my-fish/blob/master/docs/Themes.md> 
