[vundle官网](https://github.com/VundleVim/Vundle.vim)
[文章はcsdnのblogを読まれましたものです](https://blog.csdn.net/u011417820/article/details/79648429)

下载vundle
```
mkdir -p ~/.vim/bundle
git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```
修改vim配置
```
syntax on
" tab宽度和缩进同样设置为4
set tabstop=4
set softtabstop=4
set shiftwidth=4

set nocompatible

" 你在此设置运行时路径
set rtp+=~/.vim/bundle/Vundle.vim

call vundle#begin()

" 在这里面输入安装的插件
" Vundle 本身就是一个插件
Plugin 'gmarik/Vundle.vim'


"所有插件都应该在这一行之前
call vundle#end()

" filetype off
filetype plugin indent on
```
---
提示：如果使用粘贴方法复制到到.vimrc发现格式混乱，可以在shell中使用cat <<END> ~/.vimrc命令，然后粘贴代码，在输出END回车即可。

“.vimrc”文件配置好后，打开vim，在命令模式输入插件安装命令:PluginInstall命令，vim就会自动安装“.vimrc”中配置的所有插件，直到vim底部出现“Done”安装完成。

---
|命令|描述|
|:--|:--|
:PluginInstall	|	安装~/.vimrc中”call vundle#begin()”到”call vundle#end()”范围内配置好的插件；
:PluginClean	|	清理已经从”call vundle#begin()”到”call vundle#end()”范围删除的插件。
:PluginUpdate	|	更新插件
:PluginSearch	|	搜索插件，如”:PluginSearch html”搜索包含html关键词的插件。

