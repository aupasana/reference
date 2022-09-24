# neovim

```vim
:set number
:set relativenumber
:set autoindent
:set tabstop=4
:set shiftwidth=4
:set smarttab
:set softtabstop=4
:set mouse=a

:set showmatch
:set incsearch
:set ignorecase
:set cursorline
:set hlsearch
:set noswapfile
:set clipboard=unnamedplus

syntax on

" Add and run :PlugInstall
" Remove and run :PlugClean
call plug#begin('~/.vim/plugged')
Plug 'preservim/nerdtree'
Plug 'iamcco/markdown-preview.nvim', { 'do': { -> mkdp#util#install() }, 'for': ['markdown', 'vim-plug']}
Plug 'vim-airline/vim-airline'
Plug 'tpope/vim-surround' 
Plug 'godlygeek/tabular'
Plug 'preservim/vim-markdown'
Plug 'wookayin/imagepaste.vim'
Plug 'lukas-reineke/indent-blankline.nvim'
Plug 'nvim-telescope/telescope.nvim'			" :checkhealth telescope
Plug 'nvim-lua/plenary.nvim'
Plug 'nvim-treesitter/nvim-treesitter'
Plug 'BurntSushi/ripgrep'
call plug#end()

syntax enable

nnoremap <C-n> :NERDTree<CR>
nnoremap <C-t> :NERDTreeToggle<CR>
nnoremap <C-f> :NERDTreeFind<CR>

nnoremap <C-s> <Plug>MarkdownPreview

:cnoremap ymd <C-R>=strftime("%Y-%m-%d")<CR>
:cnoremap tmp <C-R>=strftime("temp/temp-%Y-%m-%d-%H-%M-")<CR>

let g:indent_guides_enable_on_vim_startup = 1
let g:vim_markdown_folding_disabled = 1

nnoremap <leader>ff <cmd>Telescope find_files<cr>
nnoremap <leader>fg <cmd>Telescope live_grep<cr>
nnoremap <leader>fb <cmd>Telescope buffers<cr>
nnoremap <leader>fh <cmd>Telescope help_tags<cr>
```
