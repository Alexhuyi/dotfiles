dotfiles 「工欲善其事，必先利其器」
==================================

Backup, restore, and sync the prefs and settings for my toolbox.

Installation
------------

#### Git, Vim, Tmux

If you are on Ubuntu x64, just run:

```
./install.sh
```

It will create three symbol links and install some essential tools.

```
from/to/dotfiles/vim/vimrc -> ~/.vimrc
from/to/dotfiles/tmux/tmux.conf -> ~/.tmux.conf
from/to/dotfiles/git/gitconfig -> ~/.gitconfig
```

If you use other Linux distribution, when you run install.sh it will prompt you to install essential tools manually.

Now you can use your brand new and amazing **vim**. The color scheme is [molokai][molokai], it works well in terminal vim(not GUI version such as GVim), I have refined molokai.vim to make molokai more monokai.

![vim screenshot](img/vim.png)

#### xShell

In menu **Tools**, open **Color Schemes** dialog, then **Import** xShell_color_scheme.xcs, select **taste** in color scheme list.

![xShell screenshot](img/xShell.png)

#### Sublime Text

Place these files in Packages/User directory.

- Windows `%HOMEPATH%\AppData\Roaming\Sublime Text 3\Packages\User`
- Linux `~/.config/sublime-text-3/Packages/User`

1. Preferences.sublime-settings ---- `Preferences > Setttings - User`
2. Package Control.sublime-settings ---- `Preferences > Package Settings > Package Control > Settings – User`, installed packages. (First install [Package Control][package-control])
3. Default(Windows).sublime-keymap ---- `Preferences > Key Bindings - User`

Workflow
--------

#### Vim (Dark Vim User)

###### 0. Vundle

- `:PluginInstall`: Installs vim plugins.
- `:PluginUpdate`: Updates vim plugins.
- `:PluginClean`: Removes unused vim plugins.

###### 1. vim-stripper

- `:Strippper`: Strips trailing whitespaces of current file or text selected in visual mode.

###### 2. NERDCommenter

- `,cc`: Comments out the current line or text selected in visual mode.
- `,cs`: Comments out the selected lines **sexily**.
- `,cu`: Uncomments the selected line(s).

###### 3. vim-flake8

- `<F7>`: Checks syntax and style for Python source code.

###### 4. YouCompleteMe and ultisnips

- `<Ctrl-n>` and `<Ctrl-p>`: Selects item in pop up menu.  
- `<Tab>`: Triggers snippet.

###### 5. nerdtree

- `<F8>`: Opens NERDTree file explorer.

###### 6. tagbar

- `<F9>`: Opens tag explorer.

###### 7. vim-easymotion

- `,,f`char: Highlights all chars and enter char to go to the char.   

###### 8. vim-fugitive

- `:Gvdiff`: To see what have changed. 

###### 9. vim-multiple-cursors
- `<Ctrl-n>, <Ctrl-p>, <Ctrl-x>`: Places multiple cursors in Normal mode.
- `c`: Changes multiple selections.
- `v`: Goes to Normal mode, `h, l`: to move cursor, `i, I, a, A` to edit.

[molokai]: https://github.com/consen/molokai
[package-control]: https://sublime.wbond.net
