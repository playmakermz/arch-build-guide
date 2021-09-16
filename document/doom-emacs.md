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
- If emacs can't open, Undefined color: "WINDOW_FOREGROUND"
```
xrdb /dev/null # type this
```
 
#### Refrences
- [How to install Doom EMACS from dtube](https://pastebin.com/Ku0bPz1U)
- [EMACS Key Bindings](https://caiorss.github.io/Emacs-Elisp-Programming/Keybindings.html)
- <https://askubuntu.com/questions/23645/how-do-i-download-the-command-line-emacs-instead-of-the-gui-one>
- <https://forums.centos.org/viewtopic.php?t=49498>
- <https://bbs.archlinux.org/viewtopic.php?id=228982/>
- <https://github.com/hlissner/doom-emacs/blob/develop/docs/getting_started.org#doom-emacs>
