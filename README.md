# FreeRDP: A Remote Desktop Protocol Implementation

This is my rdp,I will play myself

# Compilation

## 编译环境
操作系统：深度 20社区版 64位 Intel处理器  
cmake version 3.13.4  
g++ (Uos 8.3.0.3-3+rebuild) 8.3.0  
git version 2.20.1  

## 工具安装
sudo apt-get install cmake  
sudo apt-get install g++  
sudo apt-get install git  

## 依赖环境
sudo apt-get install build-essential git-core cmake libssl-dev libx11-dev libxext-dev libxinerama-dev libxcursor-dev libxdamage-dev libxv-dev libxkbfile-dev libasound2-dev libcups2-dev libxml2 libxml2-dev libxrandr-dev libavutil-dev libavcodec-dev libcunit1-dev libdirectfb-dev xmlto doxygen libxtst-dev uuid-dev libudev-dev  libusb-1.0 libdbus-glib-1-dev  
以上安装的依赖，有些个别的可能因为会下载不下来导致整个安装失败，所以这些依赖您可以分单个安装。

## 编译rdp
git clone https://github.com/StrokeAce/YouboxRdp.git  
tar cvfz ./YouboxRdp.tar.gz ./YouboxRdp/  
cd YouboxRdp  
vi ./channels/urbdrc/ChannelOptions.cmake  
将 set(OPTION_CLIENT_DEFAULT OFF) 改为 set(OPTION_CLIENT_DEFAULT ON)  
mkdir build  
cd build  
cmake ..  
make  
make DESTDIR=/opt/YouboxRDP install  
这个install也可不指定安装目录

# Run
xfreerdp /u:15229349746 /p:349746 /w:1366 /h:768 /v:61.184.241.30:25788 /d:src /cert-ignore -sec-nla  
/u:账号  
/p:密码  
/v:远程地址  
/d:控域  
