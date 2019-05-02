# MyGtkChatRoom
## 本软件基于Linux下的  codeblocks + GTK+-3.0 + glade3 + C语言 开发的及时通讯软件

### 1.Linux系统中安装GTK+工具包（基于Ubuntu18.4）
- 之前准备工作 sudo apt-get update 对安装源更新   
- 第一步确保Linux或者虚拟机中装好了C语言环境（gcc/g++等编译工具）可以使用如下命令 sudo apt-get install build-essential
- 第二步安装GTK+3.0 
      ①Linux中使用如下命令 sudo apt-get install libgtk-3-dev  ②安装项目管理工具 sudo apt-get install pkg-config  ③（选择安装）GTk帮助文档 sudo apt-get install devhelp 
- 第三步安装后确认
     确认pkg版本 pkg-config --version   确认GTK+版本  pkg-config --modversion gtk+-3.0
### 2.安装代码编辑环境 codeblocks 
    vim编辑器没有代码补全也没有错误提示。这个不多说，况且该IDE可以直接新建GTK+项目；
    sudo apt-get install codeblocks
### 3.安装glade3
    glade3可以创建图形界面，手动绘制。
    将文件保存成GTKbuilder形式（本质是XML文件），在c语言代码中可以直接获取对象。
    sudo apt-get install glade
### 4.配置IDE环境变量
     进入codeblocks中创建project选择GTK+项目，之后需要配置编译路径，
     右键项目 → build options → （compiler 中的other   ，linker中的other）两个地方添加如下语句
     `pkg-config --libs --cflags gtk+-3.0`
## glade3 的简单使用
glade是一个gtk的画图工具，该软件允许使用拖拽控件的方式进行界面布局设计，该软件有多种布局方式比如相对布局，表格布局等，控件也有很多种类型，该工具的原理就是将布局保存为一个xml文件，利用gtk+内置的GTKBuilder函数，进行对布局控件的读取，然后加以调用。并且还可以绑定signal，实现button的点击事件等。
需要注意的主要就是，在glade中需要将文件保存为GTKBuilder的形式，然后需要用

```
//获取 Builder
GtkBuilder *builder;
//填写文件的路径
 gtk_builder_add_from_file(builder,"/home/lmm/文档/login.glade", NULL );

```
最后给出官方文档：
GTK+：(https://developer.gnome.org/gtk3/stable/gtk-getting-started.html)
中道崩殂，改用QT编写，详情戳[第六组聊天室Group6ChatRoom](https://github.com/bjdlbg/Qt)
