# Install doom-emacs
 for KDE desktop environtment
 
 1. Install dependencies
 ```
# required dependencies
pacman -S git emacs ripgrep
# optional dependencies
pacman -S fd
```
2. Install doom emacs
```
git clone https://github.com/hlissner/doom-emacs ~/.emacs.d
~/.emacs.d/bin/doom install
```
3. After installing, try to refresh
```
~/.emacs.d/bin/doom sync  
~/.emacs.d/bin/doom upgrade
~/.emacs.d/bin/doom doctor # diagnosis doom
~/.emacs.d/bin/doom purge # his command from time to time to delete old, orphaned packages
```
4. Open emacs in terminal
```
emacs -nw
echo alias emacs=\"emacs -nw\" >> ~/.bashrc # make CLI emacs as default
echo alias emacs=\"emacs -nw\" >> ~/.config/fish/config.fish # make doom emacs cli as default in fish shell
```
## Start doom emacs

- If emacs can't open, Undefined color: "WINDOW_FOREGROUND"
```
xrdb /dev/null # type this
```

- Configure doom emacs
```
# ~/.doom.d/init.el  simple configure, just uncomment selected application
~/.emacs.d/bin/doom sync # after make change, don't forget to refresh emacs
```

### Key bindings
- `spc f f` Search file
- `q` quit buffer 
- `ctrl v` yank
- `spc h b b` help section keybinding
- `spc f p` Find file in private config
- `spc q r` Restart emacs
- `l and h` Open file in dired (dired +icons +ranger)
- `spc b B` switch buffer
- `spc f s` Save file
- `spc b k` kill all buffer
- `spc b d` kill selected buffet
- `spc o t` open terminal
- `spc h t` load and select theme
- `spc h d h` open documentation
- `spc h d s` list DOOM modules

### Key binding vim
- `:e DIR` edit file
- `:wq` save file

#### Set theme as default
open config.el, change doom theme as you like ( doom theme name, you can find with `spc h t` )
 
#### Refrences
- [Emacs doom cheatsheat](https://naghdbishi.ir/Doom-Emacs-Cheat-Sheet/README.html#org7d3274f)
- [Emacs key binding helpher](https://emacs.stackexchange.com/questions/63752/keybindings-for-doom-emacs)
- [Doom-emacs key Bindings](https://github.com/hlissner/doom-emacs/blob/develop/modules/config/default/%2Bevil-bindings.el)
- [How to install Doom EMACS from dtube](https://pastebin.com/Ku0bPz1U)
- [EMACS Key Bindings](https://caiorss.github.io/Emacs-Elisp-Programming/Keybindings.html)
- http://fishshell.com/docs/current/tutorial.html#:~:text=Unlike%20other%20shells%2C%20fish%20has,name%2C%20and%20then%20its%20value.
- https://www.youtube.com/watch?v=E_NP40OsxZk
- <https://lordgrenville.github.io/posts/Emacs/>
- <https://askubuntu.com/questions/23645/how-do-i-download-the-command-line-emacs-instead-of-the-gui-one>
- <https://forums.centos.org/viewtopic.php?t=49498>
- <https://bbs.archlinux.org/viewtopic.php?id=228982/>
- <https://github.com/hlissner/doom-emacs/blob/develop/docs/getting_started.org#doom-emacs>
