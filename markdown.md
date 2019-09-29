vim配置md插件
-
1. vimrc插件
```
Plugin 'godlygeek/tabular'
Plugin 'plasticboy/vim-markdown'
```
>tabular插件必须在vim-markdown之前

2. 运行插件
```
:so ~/.vimrc
:PluginInstall
```
3. 调教一下
```
let g:vim_markdown_folding_disabled = 1  #不折叠显示，默认是折叠显示，看个人习惯
let g:vim_markdown_override_foldtext = 0  
let g:vim_markdown_folding_level = 6    #可折叠的级数，对应md的标题级别
let g:vim_markdown_no_default_key_mappings = 1
let g:vim_markdown_emphasis_multiline = 0
set conceallevel=2
let g:vim_markdown_frontmatter=1
syntax on     #必须设置，否则md标记不能高亮显示
```

4. 运行
	* :Toc :Toch :Toct :Tocv
	* [实施预览 参考文档 此处有好几种 只尝试了一种](https://www.jianshu.com/p/24aefcd4ca93)
	* nodejs新版本+npm  用`npm -g install instant-markdown-d` 再弄一下插件`Plugin 'suan/vim-instant-markdown' 

---

>```和``` 两个之间的内容 -->代码

>上面内容 下一行-     ->加大字号

>#不行了吗
```
[提示文字](http://www.baidu.com)
![图片](http://图片的连接)
```
```
无序列表     *或+或-   #三种一样
有序列表     数字加.  例如：1.   #只需要第一个项目编号 后面的不太重要了

#如果在单一列表项中包含了其他东西，为了保证渲染正常，*与段落首字母之间必须保留四个空格或一个Tab
*    前面有四个空格
	>这样可以了吧
```
```
---或者***都是分割线
*这里是斜体*
_这里是斜体_

**这里是加粗**
__这里是加粗__
```
> 一个`包裹 是行内代码  两个及以上 是整段的代码

```#这里是表格处理
表头|条目一|条目二           #标题
:---:|:---:|:---:            #这一行是决定对齐 冒号在那边就是那边对齐
项目|项目一|项目二
```
```
#竟然还有转移符！！！
\   反斜线			`   反引号			*   星号
_   底线			{}  花括号			[]  方括号()  括弧
#   井字号			+   加号			-   减号
.   英文句点		!   惊叹号
```
