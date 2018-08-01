# vim-YCM

Use YouCompleteMe with vim, for autocomplition features for
C and C++. 

---

Step-1: Modify the `~/.vimrc` file and add:
```
set nocompatible
set rtp+=~/.vim/bundle/Vundle.vim

call vundle#begin()
Plugin 'VundleVim/Vundle.vim' 
Plugin 'Valloric/YouCompleteMe'
call vundle#end()
```

---

Step-2: Clone git-repos:
```
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

---

Step-3: Type vim, and hit the following:
```
:PluginInstall
```

When you see `Done` at the botton of the screen, hit `:q`

---

Step-4: Install YouCompleteMe:
```
cd ~/.vim/bundle/YouCompleteMe
sudo ./install.py --clang-completer
```

---

Step-5: Create a file `~/.vim/bundle/YouCompleteMe/.ycm_extra_conf.py`
and write the following:
```
def FlagsForFile( filename, **kwargs ):
  return {
    'flags': [ '-x', 'c++', '-Wall', '-Wextra', '-Werror' ],
  }
```

---

Enjoy autocomplete on vim...
