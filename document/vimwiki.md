# Vimwiki 
wiki plugin for vim, it's easy to write documentation and access. just type enter then link will be automatically added.

## add plugin 
add `Plug 'vimwiki/vimwiki'` in vimrc

## add settings
add this code in vimrc
```
set nocompatible
filetype plugin on
syntax on
```

## vimwiki syntax
```
= Header1 =
== Header2 ==
=== Header3 ===


*bold* -- bold text
_italic_ -- italic text

[[wiki link]] -- wiki link
[[wiki link|description]] -- wiki link with description
```
## vimwiki  list
```
* bullet list item 1
    - bullet list item 2
    - bullet list item 3
        * bullet list item 4
        * bullet list item 5
* bullet list item 6
* bullet list item 7
    - bullet list item 8
    - bullet list item 9

1. numbered list item 1
2. numbered list item 2
    a) numbered list item 3
    b) numbered list item 4
```
## open help
```
:h vimwiki-syntax
```

## External link
- https://github.com/vimwiki/vimwiki
