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
- `ctrl + v` yank
- `spc + h + b + b` help section keybinding
- 
 
#### Refrences
- [Emacs key binding helpher](https://emacs.stackexchange.com/questions/63752/keybindings-for-doom-emacs)
- [Doom-emacs key Bindings](https://github.com/hlissner/doom-emacs/blob/develop/modules/config/default/%2Bevil-bindings.el)
- [How to install Doom EMACS from dtube](https://pastebin.com/Ku0bPz1U)
- [EMACS Key Bindings](https://caiorss.github.io/Emacs-Elisp-Programming/Keybindings.html)
- <https://lordgrenville.github.io/posts/Emacs/>
- <https://askubuntu.com/questions/23645/how-do-i-download-the-command-line-emacs-instead-of-the-gui-one>
- <https://forums.centos.org/viewtopic.php?t=49498>
- <https://bbs.archlinux.org/viewtopic.php?id=228982/>
- <https://github.com/hlissner/doom-emacs/blob/develop/docs/getting_started.org#doom-emacs>
