# .vimrc configuration

### Vundle 설정

```vimrc
set nocompatible
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

Plugin 'VundleVim/Vundle.vim'

" Plugin 'The-NERD-Tree' "NERD-Tree
Plugin 'scrooloose/nerdtree'
Plugin 'jistr/vim-nerdtree-tabs'

" colorscheme
Plugin 'nanotech/jellybeans.vim'
Plugin 'altercation/vim-colors-solarized'

call vundle#end()
filetype plugin indent on
```

### Syntax Highligting 설정

```
if has("syntax")
	syntax on
endif
```
### Indent 설정

```
set autoindent
set cindent
set smartindent
set smarttab
set expandtab
```

### swp 파일 생성하지 않기

```
set nobackup "no backup file
```

### 탭사이즈 조절

```
set shiftwidth=2 "auto indent size
set ts=2 "tab size
```

### 줄 번호 표시

```
set nu
```

### 상태바 설정

```
set laststatus=2
set statusline=\ %<%l:%v\ [%P]%=%a\ %h%m%r\ %F\
set ruler
set title
```

### backspace 사용시 줄이동

```
set bs=indent,eol,start
```
```
set showcmd
```
### 검색 시 하이라이트

```
set hlsearch
```
```
:syntax on
```

### NerdTree에서 창 이동시 컨트롤 + (h,j,k,l) 사용

```
" =================
"	General Settings
" =================

" use ctrl to move

map <C-h> <C-w>h
map <C-j> <C-w>j
map <C-k> <C-w>k
map <C-l> <C-w>l
```

### 시프트 누르지 않고 `:` 입력

```
"don't use shift
map ; :
```

### vi tap 관리

```
" Key mappings
nnoremap <F9> :tabnew<CR>
nnoremap <F10> :tabclose<CR>
nnoremap <tab> :tabnext<CR>
nnoremap <S-tab> :tabprevious<CR>
```

### pane 사이즈 조절

```
nnoremap - :vertical res -5<CR>
nnoremap = :vertical res +5<CR>
nnoremap _ :res -10<CR>
nnoremap + :res +10<CR>
```

### vim 실행시 자동으로 NerdTree 실행

```
" Nerdtree setting
let g:nerdtree_tabs_open_on_console_startup = 1
let g:nerdtree_tabs_autoclose = 1
map <C-u> :NERDTreeTabsToggle<CR>
```
### 컬러스킴 사용

```
" colorscheme jellybeans
colorscheme jellybeans
```