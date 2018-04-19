# Sublime-text3的安装和使用
## Sublime text3安装
### Sublime text3的首次安装可以到指定官方网站下载，尽量使用原版，没必要使用中文版。
    [下载地址](http://www.sublimetext.com/)
 下载完成后就是傻瓜式的安装了，没什么难度，就不说明了。主要的重点就是插件这块，Sublime最强大之处就是其插件的数量足够多
    
## Sublime插件安装
### 首次安装插件需进行配置工作，具体步骤如下：
1. 优先配置Package control组件（[说明](https://packagecontrol.io/installation)）
  * 按Ctrl+ `调出console
  * 按下载sublime版本text2或者text3，粘贴相应的代码到命令行并回车
  * 重启sublime即可
  * 打开Perferences->package settings中看到package control这一项，则表示安装成功，接下来就可以用Package Control安装插件了
2. 快捷键按下Ctrl+shift+p,调出命令面板，输入ipc,找到install package选项并回车，就可以输入对于的插件名称进行安装了

### 比较高效有用的插件列表
1. Soda Theme
   Sublime Text 3中较为常用的一款自定义编辑器主题，用过的人都说好。Soda Theme包含代码着色、标签、图标，拥有light和dark两种颜色主题便于用户在不同时间段使用。
2. Alignment
  Aligment插件让开发者自动对齐代码，包括PHP、CSS、JavaScript语言。使得代码看起来更整齐美观，更具可读性。
3. SublimeLinter
  一个支持lint语法的插件，可以高亮linter认为有错误的代码行，也支持高亮一些特别的注释，比如“TODO”，这样就可以被快速定位。
4. Ctags
  代码跳转，Ctags是一个用于从程序源代码树产生索引文件（或tag文件)，从而便于文本编辑器来实现快速定位的实用工具。在产生的tag文件中，每一个tag的入口指向了一个编程语言的对象
5. sftp(部署代码到服务器)
  一键部署代码到服务器，方便快捷。
6. FileHeader
   在创建新文件时自动添加文件模板
7. sublime本地编译运行
   直接按ctrl+B实现lua文件的编译运行
8. LuaKit语法提示插件
   实现对代码内变量名，方法的自动提示功能
   
## sublime Text3的必要快捷键
### 选择类
* Ctrl+D 选中光标所占的文本，继续操作则会选中下一个相同的文本。
* Alt+F3 选中文本按下快捷键，即可一次性选择全部的相同文本进行同时编辑。举个栗子：快速选中并更改所有相同的变量名、函数名等。
* Ctrl+L 选中整行，继续操作则继续选择下一行，效果和 Shift+↓ 效果一样。
* Ctrl+Shift+L 先选中多行，再按下快捷键，会在每行行尾插入光标，即可同时编辑这些行。
* Ctrl+Shift+M 选择括号内的内容（继续选择父括号）。举个栗子：快速选中删除函数中的代码，重写函数体代码或重写括号内里的内容。
* Ctrl+M 光标移动至括号内结束或开始的位置。
* Ctrl+Enter 在下一行插入新行。举个栗子：即使光标不在行尾，也能快速向下插入一行。
* Ctrl+Shift+Enter 在上一行插入新行。举个栗子：即使光标不在行首，也能快速向上插入一行。
* Ctrl+Shift+[ 选中代码，按下快捷键，折叠代码。
* Ctrl+Shift+] 选中代码，按下快捷键，展开代码。
* Ctrl+K+0 展开所有折叠代码。
* Ctrl+← 向左单位性地移动光标，快速移动光标。
* Ctrl+→ 向右单位性地移动光标，快速移动光标。
* shift+↑ 向上选中多行。
* shift+↓ 向下选中多行。
* shift+← 向左选中文本。
* shift+→ 向右选中文本。
* Ctrl+Shift+← 向左单位性地选中文本。
* Ctrl+Shift+→ 向右单位性地选中文本。
* Ctrl+Shift+↑ 将光标所在行和上一行代码互换（将光标所在行插入到上一行之前）。
* Ctrl+Shift+↓ 将光标所在行和下一行代码互换（将光标所在行插入到下一行之后）。
* Ctrl+Alt+↑ 向上添加多行光标，可同时编辑多行。
* Ctrl+Alt+↓ 向下添加多行光标，可同时编辑多行。

### 编辑类
* Ctrl+J 合并选中的多行代码为一行。举个栗子：将多行格式的CSS属性合并为一行。
* Ctrl+Shift+D  复制光标所在整行，插入到下一行。
* Tab 向右缩进。
* Shift+Tab 向左缩进。
* Ctrl+K+K 从光标处开始删除代码至行尾。
* Ctrl+Shift+K 删除整行。
* Ctrl+/ 注释单行。
* Ctrl+Shift+/ 注释多行。
* Ctrl+K+U 转换大写。
* Ctrl+K+L 转换小写。
* Ctrl+Z 撤销。
* Ctrl+Y 恢复撤销。
* Ctrl+U 软撤销，感觉和 Gtrl+Z 一样。
* Ctrl+F2 设置书签
* Ctrl+T 左右字母互换。
* F6 单词检测拼写

### 搜索类（重点！！！）
* Ctrl+F 打开底部搜索框，查找关键字。
* Ctrl+shift+F 在文件夹内查找，与普通编辑器不同的地方是sublime允许添加多个文件夹进行查找，略高端，未研究。
* Ctrl+P 打开搜索框。举个栗子：1、输入当前项目中的文件名，快速搜索文件，2、输入@和关键字，查找文件中函数名，3、输入：和数字，跳转到文件中该行代码，4、输入#和关键字，查找变量名。
* Ctrl+G 打开搜索框，自动带：，输入数字跳转到该行代码。举个栗子：在页面代码比较长的文件中快速定位。
* Ctrl+R 打开搜索框，自动带@，输入关键字，查找文件中的函数名。举个栗子：在函数较多的页面快速查找某个函数。
* Ctrl+： 打开搜索框，自动带#，输入关键字，查找文件中的变量名、属性名等。
* Ctrl+Shift+P 打开命令框。场景栗子：打开命名框，输入关键字，调用sublime text或插件的功能，例如使用package安装插件。
* Esc 退出光标多行选择，退出搜索框，命令框等。


### sublime + lua的实现
1. lua环境的配置：
  * window环境下首先务必安装luaForWindow,即可完成所有lua环境的配置，不需要配置环境变量
  * mac环境下lua的安装配置：
  
    ```
    curl -R -O http://www.lua.org/ftp/lua-5.2.3.tar.gz
    tar zxf lua-5.2.3.tar.gz
    cd lua-5.2.3
    make macosx test
    ```
    
2. sublime text3工具新增lua的配置：
  * 在Tools下选择Build System下的new Build System,输入
  
  ```
   {  
    "cmd": ["E:\\lua\\5.1\\lua.exe", "$file"],  
    "file_regex": "^(...*?):([0-9]*):?([0-9]*)",  
    "selector": "source.lua",
    }  
  ```
  
  并执行保存。
  * 在Tools下选择Build System选择刚才保存的文件名
  * 之后每次编译只需要按住ctrl + b即可
