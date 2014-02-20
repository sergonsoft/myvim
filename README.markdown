This is a tipical .vimrc file I use

## .vimrc

    " Copywrite 2014 Sergey
    
    " установка вида и размера шрифта
    set guifont=Menlo\ Regular:h14
    
    " установка количества символов в строке (ширина окна терминала)
    "set columns=83
    
    " установка количества линий (высота окна терминала)
    "set lines=40
    
    " отображать номера строк
    set number
    
    " пробовать применять следующие кодировки при при открытии файла
    set fileencodings=ucs-bom,utf-8,default,cp1251,latin1
    
    set expandtab
    "set textwidth=79
    set tabstop=8
    set softtabstop=4
    set shiftwidth=4
    set autoindent
    
    set colorcolumn=79

    " выполнить динамическое построение путей для поиска подключаемых плагинов для Vim
    runtime bundle/vim-pathogen/autoload/pathogen.vim
    call pathogen#infect()
    call pathogen#helptags()
    
    set foldmethod=indent
    set foldlevel=99
    
    syntax on
    filetype on
    filetype plugin indent on
    
    map <leader>td <Plug>TaskList
    
    let g:pyflakes_use_quickfix = 0
    
    let g:pep8_map='<leader>8'
    
    autocmd FileType python set omnifunc=pythoncomplete#Complete
    let g:SuperTabDefaultCompletionType = "context"
    
