## SpaceVim 
recommended ```pacman -S gvim ``` ,
``` curl -sLf https://spacevim.org/install.sh | bash ```, ```ls | grep 'ls'```
+ install ``` pip install --user pynvim```

location .SpaceVim.d/init.toml
```
#=============================================================================
# basic.toml --- basic configuration example for SpaceVim
# Copyright (c) 2016-2020 Wang Shidong & Contributors
# Author: Wang Shidong < wsdjeg at 163.com >
# URL: https://spacevim.org
# License: GPLv3
#=============================================================================

# All SpaceVim option below [option] section
[options]
    # set spacevim theme. by default colorscheme layer is not loaded,
    # if you want to use more colorscheme, please load the colorscheme
    # layer, the value of this option is a string.
    colorscheme = "afterglow"
    colorscheme_bg = "dark"
    # Disable guicolors in basic mode, many terminal do not support 24bit
    # true colors, the type of the value is boolean, true or false.
    enable_guicolors = true
    # Disable statusline separator, if you want to use other value, please
    # install nerd fonts
    statusline_separator = "nil"
    statusline_iseparator = "bar"
    buffer_index_type = 4
    # Display file type icon on the tabline, If you do not have nerd fonts
    # installed, please change the value to false
    enable_tabline_filetype_icon = true
    # Display current mode text on statusline, by default It is disabled,
    # only color will be changed when switch modes.
    enable_statusline_mode = true
    bootstrap_before = 'myspacevim#before'
    bootstrap_after = 'myspacevim#after'


# Enable autocomplete layer
[[layers]]
name = 'autocomplete'
auto_completion_return_key_behavior = "complete"
auto_completion_tab_key_behavior = "cycle"

[[layers]]
name = "default"

[[layers]]
name = 'shell'
default_position = 'top'
default_height = 30

[[layers]]
name = 'format'
format_on_save = true

[[layers]]
name = "lang#html"
format_on_save = true

[[layers]]
name = 'lang#python'
format_on_save = true

[[custom_plugins]]
repo = 'danilo-augusto/vim-afterglow'
merged = false

[[custom_plugins]]
repo = 'Shougo/vimproc.vim'
merged = false

```
#### spacevim bootstrap
```
function! myspacevim#before() abort
let g:spacevim_relativenumber = 0
endfunction

function! myspacevim#after() abort
endfunction

" area .SpaceVim.d/autoload/myspacevim.vim 
```
#### Emmet start
``` ctrl + e + , ```
#### start and enable
1. SPUpdate , 2. SPInstall , 3.  keluar dan masuk kembali
#### neovim dan clipboard
```yay -S neovim-gtk ``` nvim cara mengunakannya ``` "+y ``` atau ```\y```
#### Format html
src <https://linux.die.net/man/1/tidy>
```tidy -m index.html```
#### recommended vim theme 
<https://github.com/dracula/vim> # ini bisa untuk vim
#### add pip package
```pip install --user pynvim```
