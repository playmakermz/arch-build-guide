## SpaceVim 
recommended ```pacman -S gvim ``` ,
- ``` curl -sLf https://spacevim.org/install.sh | bash ``` # install both vim and neovim
- ` curl -sLf https://spacevim.org/install.sh | bash -s -- --uninstall` uninstall spacevim
- `curl -sLf https://spacevim.org/install.sh | bash -s -- -v` spacevim version
## Requirement
- `pacman -S neovim vim gvim lua python-pip`
- `sudo apt install vim-gtk3` # if you using debian based
- `yay -S neovim-gtk vim-gtk-recent-git`
- `pip install --user pynvim pylint yapf autoflake isort overage`

## Key-binding
- `spc f v d` open init.toml
- `\y` atau `"+y` copy to clipboard
- `:SPUpdate` update spacevim
- `SPInstall` Install plugin
- `spc '` open terminal
- `spc f t` open file tree

## Open HTML in CLI browser
type `w3m index.html` in terminal.

## auto line break 
src: https://stackoverflow.com/questions/9131271/vim-auto-line-break

`:set tw=80`


## edit init.toml
location .SpaceVim.d/init.toml
<details> <summary> SpaceVim My config </summary>
    
### Source-code :
    
```
#=============================================================================
# basic.toml --- basic configuration example for SpaceVim
# Copyright (c) 2016-2020 Wang Shidong & Contributors
# Author: Wang Shidong < wsdjeg at 163.com >
# URL: https://spacevim.org
# License: GPLv3
#=============================================================================

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
    colorscheme = "dracula"
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
    #disabled_plugins = ['emmet-vim']
    filemanager = 'nerdtree'


# Enable autocomplete layer
[[layers]]
name = 'autocomplete'
auto_completion_return_key_behavior = "complete"
auto_completion_tab_key_behavior = "cycle"

# copy paste to clipboard
[[layers]]
name = "default"

# start shell spc '
[[layers]]
name = 'shell'
default_position = 'top'
default_height = 30

# format file, 
[[layers]]
name = 'format'
enable = true
format_on_save = true

# version control GIT
[[layers]]
  name = "git"
  git_plugin = 'fugitive'

# emmet 
[[layers]]
name = "lang#html"
emmet_leader_key = "<c-e>"
emmet_filetyps = ['html']

# Python 
[[layers]]
name = 'lang#python'

# check mistake
[[layers]]
name = "checkers"
show_cursor_error = false # untuk bisa mengunakan fitur ini, hidupkan dulu

# autocomplete
[[layers]]
  name = "autocomplete"

# colorscheme
[[layers]]
  name = "colorscheme"

# file tree 
[[layers]]
    name = 'core'
    filetree_show_hidden = true
    enable_smooth_scrolling = true
    filetree_opened_icon = ''
    filetree_closed_icon = ''

# sudo. start spc f w. using 
[[layers]]
  name = "sudo"

# tmux 
[[layers]]
  name = "tmux"
  tmux_navigator_modifier = "alt"

[[layers]]
  name = "ui"

# bookmark
[[layers]]
name = 'tools'

# ======================== Custom plugins
[[custom_plugins]]
repo = 'joshdick/onedark.vim'
merged = false

#[[custom_plugins]]
#repo = 'mattn/emmet-vim'
#merged = false

[[custom_plugins]]
  repo = "dracula/vim"
  name = "dracula"
  merged = false


```
## spacevim bootstrap
```
function! myspacevim#before() abort
" let g:spacevim_relativenumber = 0
let g:user_emmet_leader_key='<c-e>'

endfunction

function! myspacevim#after() abort
endfunction

" area .SpaceVim.d/autoload/myspacevim.vim 
```
</details>    

#### Emmet start
``` ctrl + e + , ```
#### start and enable
1. SPUpdate , 2. SPInstall ,
#### Format html
src <https://linux.die.net/man/1/tidy>
```tidy -im index.html```
#### recommended vim theme 
<https://github.com/dracula/vim> 

## Pranala
- https://draculatheme.com/vim
- https://github.com/SpaceVim/SpaceVim/blob/master/docs/install.sh
- https://github.com/mattn/emmet-vim
- https://www.fosslinux.com/18554/how-to-access-website-using-command-line-from-the-terminal.htm

