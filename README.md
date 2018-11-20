# MyGtkChatRoom
Linux下GTK+及时通讯软件
### 本软件基于Linux下的  codeblocks + GTK+-3.0 + glade3 + C语言 开发的及时通讯软件
之前准备工作
## 1.Linux系统中安装GTK+工具包（基于Ubuntu18.4）
  第一步确保Linux或者虚拟机中装好了C语言环境（gcc/g++等编译工具）可以使用如下命令 
                    sudo apt-get install build-essential
  第二步安装GTK+3.0 ①Linux中使用如下命令 sudo apt-get install libgtk-3-dev
                   ②安装项目管理工具 sudo apt-get install pkg-config
                   ③（选择安装）GTk帮助文档 sudo apt-get install devhelp 
  第三步安装后确认  确认pkg版本 pkg-config –version   确认GTK+版本  pkg-config –modversion gtk+-3.0
