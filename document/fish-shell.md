## Install And configure Fish Shell

Using fish shell to make Terminal more beautiful

```
curl -L https://get.oh-my.fish > install
fish install --path=~/.local/share/omf --config=~/.config/omf
# (optional) Configure your terminal. to always use fish shell
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
## to make this option always default
vim ~/.config/fish/config.fish  
## inside config.fish
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
Set `/usr/bin/fish` inside console profile 'command' form
#### refrensi 
<https://github.com/oh-my-fish/oh-my-fish> <br> <https://github.com/oh-my-fish/oh-my-fish/blob/master/docs/Themes.md> <br> <https://fishshell.com/docs/current/>
