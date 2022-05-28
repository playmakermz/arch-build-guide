## Install And configure Fish Shell

Using fish shell to make Terminal more beautiful

```
curl -L https://get.oh-my.fish > install
fish install --path=~/.local/share/omf --config=~/.config/omf
# (optional) Configure your terminal. to always use fish shell
```
atau 
`curl https://raw.githubusercontent.com/oh-my-fish/oh-my-fish/master/bin/install | fish`
## Install theme and use theme
```
omf install bobthefish
omf install ocean
omf theme bobthefish
omf list
```
## select theme for bobthefish
lokasi `vim ~/.config/fish/config.fish`
```
## to make this option always default
## inside config.fish
if status is-interactive
# Commands to run in interactive sessions can go here
set theme_color_scheme neolambda
end
```
opsi color_scheme = `flash`

## Delete theme
```
omf remove themename
```
## Konsole ( kde terminal )
set fish to default use
Set `/usr/bin/fish` inside console profile 'command' form
#### refrensi 
- <https://github.com/oh-my-fish/oh-my-fish> 
- <https://github.com/oh-my-fish/oh-my-fish/blob/master/docs/Themes.md> 
- <https://fishshell.com/docs/current/>
- https://askubuntu.com/questions/300832/run-same-command-again-but-as-root
- [ Set Fish shell as default ](https://askubuntu.com/questions/26439/how-do-i-set-fish-as-the-default-shell)
- [set fish as default shell, has been tested in chromebook](https://tech.davidfield.co.uk/2021/03/18/supercharge-your-chromebook-linux-shell/)
