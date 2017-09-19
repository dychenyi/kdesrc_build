# kdesrc_build
how to compile kdesrc in centos. Take notes in github :)

1) install qt, cmake, perl  setup env. 
tar Jxvf xxx.tar.xz  
//解压xz文件

yum install gcc-c++ 
//安装g++

yum install mesa-libGL-devel mesa-libGLU-devel freeglut-devel   
//安装opengl

yum search/ yum list xxxx  
//搜索包

setenv TCL_LIBRARY=tcl安装目录
//tcl 环境设置

setenv LD_LIBRARY_PATH=glibc目录/lib:$LD_LIBRARY_PATH  
//glibc  环境设置

2) This is my cshrc.
setenv LD_LIBRARY_PATH /home/chenyi/DEV/Qt/5.9.1/gcc_64/lib:/home/chenyi/DEV/tcl/lib:/usr/lib:/usr/lib64    
set path= ( $path /home/chenyi/DEV/Qt/5.9.1/gcc_64/bin/  /home/chenyi/DEV/Qt/Tools/QtCreator/bin /usr/bin/ 
/home/chenyi/DEV/cmake-3.9.1/bin /home/chenyi/DEV/tcl/bin /opt/ActivePerl-5.24/bin/)
setenv ECM_DIR /home/chenyi/DEV/cmake-3.9.1/Modules/extra-cmake-module

3) https://kdesrc-build.kde.org/ 
Latest Release:: The development version of kdesrc-build is currently recommended, and can be downloaded from KDE's git server by running: $ git clone git://anongit.kde.org/kdesrc-build

This command will download kdesrc-build (the script and its associated modules) and sample configuration files suitable for KDE Frameworks 5 and Plasma Desktop 5. Afterwards, you can runkdesrc-build --metadata-only

4) A lot of errors occurs while compiling. yum list xxx & yum install xxx . Then is OK. And finally KDE building costs a lot of time!

