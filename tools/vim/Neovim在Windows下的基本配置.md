* 添加 bin 到环境变量

* 配置文件 init.vim 放在 ~/AppData/Local/nvim

* 添加拼写检查的字典

  * `:set spell` 如果报错, 或者提示没权限, 则手动创建目录 ~/AppData/Local/nvim/site/spell 和 ~/AppData/Local/nvim/spell
  * 下载字典文件 https://github.com/vim/vim/blob/master/runtime/spell/en.utf-8.spl 和 https://github.com/vim/vim/blob/master/runtime/spell/en.utf-8.sug, 把它们放到那两个目录(各放两个好了, 忘了怎么回事去了)

* 改下配置文件里 bash 路径 `set shell=C:/Devtools/Git/bin/bash.exe`

* 添加 python 支持

  * `pip2 install -i https://pypi.tuna.tsinghua.edu.cn/simple neovim`
  * `pip3 install -i https://pypi.tuna.tsinghua.edu.cn/simple neovim`

* 设置 python 路径

  * `let g:python3_host_prog='C:/Devtools/Python3/python.exe'`
  * `let g:python_host_prog='C:/Devtools/Python2/python.exe'`

* 添加 ruby 支持

  * `gem install neovim`

* 设置 ruby 路径

  * `let g:ruby_host_prog='C:/Devtools/Ruby24/bin/ruby.exe'`

* 添加 node 支持

  * `npm i -g neovim`

* 设置 node 路径

  * `let g:node_host_prog  = 'C:\Devtools\Nodejs\node.exe'`

* 检查各项支持是否 OK `:CheckHealth` 或者单独检查 python `:echo has("python3")` (返回 1 OK)等等

* 安装 vim-plug, 到 Github 下载 plug.vim, 放到 ~/AppData/Local/nvim/autoload/plug.vim

  * ```
    call plug#begin('~/.vim/plugged')
    Plug 'mattn/emmet-vim'
    Plug 'scrooloose/nerdtree'
    ...
    call plug#end()

    ```

* 配置其他插件

* 如果用 Vim 的话, 可在 https://github.com/micbou/vim-for-windows 或 https://tuxproject.de/projects/vim/ 找到预编译的支持 py2, py3 的二进制文件, 不用加环境变量, 记得在 git bash 的 git-prompt.sh 或者 aliases.sh 中加个 alias 就好, 不过 Neovim 也得有个, 给 VSCode 用

* 记得改下 Ultisnips 的 snippet