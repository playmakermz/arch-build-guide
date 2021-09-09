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
## Konsole ( kde terminal )
set fish to default use
`vim /etc/shells # add /usr/bin/fish`
`chsh -s /usr/bin/fish`
`/usr/bin/fish # in konsole profile`
#### refrensi 
<https://github.com/oh-my-fish/oh-my-fish> <br> <https://github.com/oh-my-fish/oh-my-fish/blob/master/docs/Themes.md> <br> <https://fishshell.com/docs/current/>
