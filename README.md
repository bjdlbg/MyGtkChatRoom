# MyGtkChatRoom
## 本软件基于Linux下的  codeblocks + GTK+-3.0 + glade3 + C语言 开发的及时通讯软件

### 1.Linux系统中安装GTK+工具包（基于Ubuntu18.4）
- 之前准备工作 sudo apt-get update 对安装源更新   
- 第一步确保Linux或者虚拟机中装好了C语言环境（gcc/g++等编译工具）可以使用如下命令 sudo apt-get install build-essential
- 第二步安装GTK+3.0 
      ①Linux中使用如下命令 sudo apt-get install libgtk-3-dev  ②安装项目管理工具 sudo apt-get install pkg-config  ③（选择安装）GTk帮助文档 sudo apt-get install devhelp 
- 第三步安装后确认
     确认pkg版本 pkg-config -–version   确认GTK+版本  pkg-config –-modversion gtk+-3.0
### 2.安装代码编辑环境 codeblocks 
    vim编辑器没有代码补全也没有错误提示。这个不多说，况且该IDE可以直接新建GTK+项目；
    sudo apt-get install codeblocks
### 3.安装glade3
    glade3可以创建图形界面，手动绘制。
    将文件保存成GTKbuilder形式（本质是XML文件），在c语言代码中可以直接获取对象。
    sudo apt-get glad
### 4.配置IDE环境变量
     进入codeblocks中创建project选择GTK+项目，之后需要配置编译路径，右键项目 → build options → （compiler 中的other   ，linker中的other）两个地方添加如下语句`pkg-config --blibs --cflags gtk+-3.0`
