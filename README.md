## Instalar ohmybash
```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"
```
### Editar bashrc
```bash
vim ~/.bashrc
OSH_THEME="agnoster"
alias vim=nvim
```
## Instalar neovim
```bash
apt install neovim
```
### Crear archivo configuracion neovim
```bash
mkdir -p  ~/.config/nvim/ && vim .config/nvim/init.vim 
```
```bash
" Plugins will be downloaded under the specified directory.
call plug#begin(has('nvim') ? stdpath('data') . '/plugged' : '~/.vim/plugged')

" Declare the list of plugins.
Plug 'tpope/vim-sensible'
Plug 'junegunn/seoul256.vim'
Plug 'scrooloose/nerdtree', { 'on':  'NERDTreeToggle' }
" List ends here. Plugins become visible to Vim after this call.
call plug#end()

set title  " Muestra el nombre del archivo en la ventana de la terminal
set number  " Muestra los números de las líneas
set mouse=a  " Permite la integración del mouse (seleccionar texto, mover el cursor)

set nowrap  " No dividir la línea si es muy larga

set cursorline  " Resalta la línea actual
set colorcolumn=120  " Muestra la columna límite a 120 caracteres

" Indentación a 2 espacios
set tabstop=2
set shiftwidth=2
set softtabstop=2
set shiftround
set expandtab  " Insertar espacios en lugar de <Tab>s

set hidden  " Permitir cambiar de buffers sin tener que guardarlos

set ignorecase  " Ignorar mayúsculas al hacer una búsqueda
set smartcase  " No ignorar mayúsculas si la palabra a buscar contiene mayúsculas

set spelllang=en,es  " Corregir palabras usando diccionarios en inglés y español

set termguicolors  " Activa true colors en la terminal
"set background=light  " Fondo del tema: light o dark
"colorscheme zellner  " Nombre del tema

```
### Aplicamos los cambios
```bash
source ~/.config/nvim/init.vim
Then install this plugin in Nvim using command :PlugInstall.
```

## LINKS
[ohmybash](https://ohmybash.nntoan.com/)

[personalizarTerminal](https://www.edevars.com/blog/personalizar-terminal)

[NERDTree](https://jdhao.github.io/2018/09/10/nerdtree_usage/)

[NERDTree2](https://github.com/preservim/nerdtree)


