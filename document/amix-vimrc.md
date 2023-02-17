# Amix-vimrc
![vim-example](../aset/example-vim.png)

[Amix-vimrc](https://github.com/amix/vimrc)

```
git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime
sh ~/.vim_runtime/install_awesome_vimrc.sh
```

install vim plug ( vim )

```
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```
install vimplug (nvim)
```
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

Install Node js 
```
sudo apt install nodejs npm
npm install n -g
sudo n stable # untuk install versi stable 
```

## Example for vimrc
- `vmap <C-c> "+y`
"For copy paste, using vim-gtk3
- `<c-e>`
For using emmet | ctrl + e + leader(,)
- `<C-x>` and `<C-n>` to start select code completion 
- `<C-n>` to find matches file 
- "Ctrl + n" for select next text auto completion
- `<c-p>` for selesct previous text auto completion
- "TAB" for sellect auto completion (supertabb)
- ":tabnew" open new tab
- "gt" move around tab
- `<c-m>` | ctrl + m for auto format 
- `<c-i>` for auto commenting

## Vim code completion
must have node js installed and vim plug 
1. Open vimrc, and add `Plug 'neoclide/coc.nvim', {'branch': 'release'}`
2. `PlugInstall`
3. open vim and type in vim console 
4. `:CocInstall coc-tsserver coc-json coc-html coc-css coc-pyright coc-snippets coc-solargraph coc-json`


## My vimrc (~/.vim_runtime/my_configs.vim)
use this path(~/.vim_runtime/my_configs.vim) not .vimrc
( .config/nvim/init.vim ) for nvim
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
Plug 'ap/vim-css-color'
Plug 'othree/html5.vim'
Plug 'NLKNguyen/papercolor-theme'
Plug 'joshdick/onedark.vim'
Plug 'neoclide/coc.nvim', {'branch': 'release'}
Plug 'nathanaelkane/vim-indent-guides'
Plug 'maksimr/vim-jsbeautify'
Plug 'ervandew/supertab'


call plug#end()


" ================ Mapping ===========

noremap! <Leader><tab> <esc>gg=G<C-o><C-o>zz 
" auto indent file 
vmap <C-c> "+y
" For copy paste, using vim-gtk3
nmap <C-q> :q! 
" Exit file 
nmap <C-s> =G
" Indentation file, move cursor to the top of file and press C-s 
imap <C-l> <esc>gcc
nmap <C-l> <esc>gcc
" Turn line into comment type
        
"============== Settings ==============
colorscheme afterglow
set background=dark

" background dark
filetype indent on
filetype on
" Highlight cursor line underneath the cursor horizontally.
set cursorline

" Highlight cursor line underneath the cursor vertically.
set cursorcolumn

" vim emmet key
let g:user_emmet_leader_key='<c-e>'

" ============= Autocompletion
filetype plugin on
set omnifunc=syntaxcomplete#Complete

" Vim Indent display
let g:indent_guides_enable_on_vim_startup = 1
let g:indent_guides_auto_colors = 1
"hi IndentGuidesOdd  ctermbg=black
"hi IndentGuidesEven ctermbg=darkgrey

" Vim JsBeautify formatter
" https://github.com/maksimr/vim-jsbeautify
".vimrc
map <c-m> :call JsBeautify()<cr>
" or
autocmd FileType javascript noremap <buffer>  <c-m> :call JsBeautify()<cr>
" for json
autocmd FileType json noremap <buffer> <c-m> :call JsonBeautify()<cr>
" for jsx
autocmd FileType jsx noremap <buffer> <c-m> :call JsxBeautify()<cr>
" for html
autocmd FileType html noremap <buffer> <c-m> :call HtmlBeautify()<cr>
" for css or scss
autocmd FileType css noremap <buffer> <c-m> :call CSSBeautify()<cr>

" refrence https://medium.com/vim-drops/css-autocompletion-on-vim-no-plugins-needed-e8df9ce079c7

" Supertabb http://eclim.org/vim/code_completion.html
let g:SuperTabDefaultCompletionType = 'context'



```

## Vim CheatSheet
- https://vim.rtorr.com/


## For more information about vim mapping
- https://www.techrepublic.com/blog/linux-and-open-source/create-custom-keybindings-in-vim/


## Refrence 
- https://github.com/neoclide/coc.nvim/wiki/Install-coc.nvim
- https://stackoverflow.com/questions/10075990/upgrading-node-js-to-latest-version
- http://eclim.org/vim/code_completion.html [ Vim code auto completion ]
