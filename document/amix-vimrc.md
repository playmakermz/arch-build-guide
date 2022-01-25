# Amix-vimrc
[Amix-vimrc](https://github.com/amix/vimrc)

`
git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime
sh ~/.vim_runtime/install_awesome_vimrc.sh
`

## Example for vimrc
`vmap <C-c> "+y`

"For copy paste, using vim-gtk3


## My vimrc (~/.vim_runtime/my_configs.vim)
use this path(~/.vim_runtime/my_configs.vim), instead .vimrc
```
call plug#begin('~/.vim/plugged')

Plug 'preservim/nerdtree'
Plug 'vim-airline/vim-airline'
Plug 'vim-airline/vim-airline-themes'
Plug 'jmcantrell/vim-virtualenv'
Plug 'danilo-augusto/vim-afterglow'
Plug 'whatyouhide/vim-gotham'
Plug 'mattn/emmet-vim'
Plug 'sheerun/vimrc'
Plug 'othree/html5.vim'
Plug 'NLKNguyen/papercolor-theme'
Plug 'joshdick/onedark.vim'

call plug#end()
" PlugUpdate / PlugInstall 

================ Mapping ===========

vmap <C-c> "+y
" For copy paste, using vim-gtk3

"============== Settings ==============
set background=dark
set syntax = on

filetype on 
" Highlight cursor line underneath the cursor horizontally.
set cursorline

" Highlight cursor line underneath the cursor vertically.
set cursorcolumn

colorscheme onedark
```

## For more information about vim mapping
- https://www.techrepublic.com/blog/linux-and-open-source/create-custom-keybindings-in-vim/



