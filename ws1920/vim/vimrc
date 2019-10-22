"
"  Approachable .vimrc
"
"  Created by Thomas Johannesmeyer (thomas@geeky.gent) on 25.09.2018.
"  Copyright (c) 2018 www.geeky.gent. All rights reserved.
"
"  Disclaimer: I tailored this .vimrc for people who are stumbling into Vim on
"  accident when using Git. Therefore I setup keybindings frowned upon in the
"  die-hard Vim community (arrow-keys).
"


set nocompatible      " Ignore VI compatibility and enter the current millenium

set term=builtin_ansi
set encoding=utf-8

set autoread          " Automatic reload on file change
set noswapfile        " Go away swp-file. No one loves you!
set noshowmode        " Disables Vim's Mode Display because we have a status bar plugin
set updatetime=250    " Updatetime interval to 250ms (default: 4000) to improve GitGutter
set cindent           " Enables C Indentation
set smartindent       " Enables Smart indentation
set autoindent        " Enables Auto indentation
set showcmd           " Show incomplete Commands
set ttyfast           " faster redrawing
set nolazyredraw      " don't redraw while executing macros
set magic             " Set magic on, for regex
set showmatch         " show matching braces
set scrolloff=8       " Always display at least n context lines when scrolling to bottom of the screen
syntax enable         " Enables syntax highlighting
set browsedir=current
set shiftwidth=2
set shiftround        " When pressing Tab at 3 spaces, go to 4 instead of 5.
set expandtab         " Replace Tabs with Spaces
set tabstop=2         " One Tab equals 2 spaces

set number            " Enable line numbers
set relativenumber    " Enables relative numbering as default

set ic                " Ignore case in search patterns

set nrformats=        " Switch from base 8 to base 10 when using <C-a>

set path+=**          " Enable recursive file search. Tab-Completion into subfolders(!)
set wildmenu          " Display all matching files when we tab complete
" These two enable us to hit tab to :find by partial match and use * to make
" it fuzzy
"
" :b lets you autocomplete any open buffer

" display indentation guides
set list listchars=tab:❘-,trail:·,extends:»,precedes:«,nbsp:×
set showbreak=▸

set smartcase " user case in search ONLY when any caps is used
set hlsearch  " highlight search
set incsearch " show matches as search proceeds


" error bells
set noerrorbells
set visualbell
set t_vb=
set tm=500


" highlight conflicts
match ErrorMsg '^\(<\|=\|>\)\{7\}\([^=].\+\)\?$'

" This enables correct coloration
if !has('gui_running')
  set t_Co=256
endif



" ==================== Keybindings ====================
" Getting rid of mishaps and annoyances
" Get out of my way K...
nnoremap K <nop>

" Avoid unintentional switches to ex mode
nmap Q q

" Arrow Keys instead of h,j,k,l
nmap <silent> <left> h
nmap <silent> <down> j
nmap <silent> <up> k
nmap <silent> <right> l

" Save & Exit Operations
" Hopefully saving you a trip to https://stackoverflow.com/questions/11828270/how-to-exit-the-vim-editor ;)
nnoremap <c-q> <Esc>:q!<CR>
nnoremap <c-s> <Esc>:write<CR>

" Press Return to enter insert mode
nnoremap <CR> <insert>


" Indent line(s) using Tabulator Key
nnoremap <Tab> >>
nnoremap <S-Tab> <<

" This mapping will re-establish block selection after indentation:
xnoremap <Tab> >gv
xnoremap <S-Tab> <gv

set mouse=a
map <ScrollWheelUp> <C-Y>
map <ScrollWheelDown> <C-E>

" ==================== German Keyboard Layout - Finding proper usecases for Umlauts ====================

" Allows you to skip paragraphs using ö and ä
noremap ö {
noremap ä }

" ==================== Leader Map ====================
let mapleader = "\<space>"  "Define Space as leader key
let maplocalleader = "," " Define localleader key
nnoremap <space> <nop>  " Unbind Space in normal mode (was bound to move cursor right)
" Unbind leader without following key functionality:
nnoremap <leader> <nop>
nnoremap <localleader> <nop>


" ==================== Style & Font ====================
highlight MatchParen ctermfg=white ctermbg=black " Highlight matching parenthesis
highlight LineNr term       = bold ctermfg = white ctermbg = black " white text, invisible background
highlight CursorLineNr term = bold ctermfg = white ctermbg = black " white text, invisible background
autocmd InsertEnter * set cul
autocmd InsertLeave * set nocul
highlight clear SignColumn
"
" adjust highlight color:
highlight Search cterm=NONE ctermfg=white ctermbg=black
