# FreeRDP: A Remote Desktop Protocol Implementation

This is my rdp,I will play myself

# Compilation

## ���뻷��
����ϵͳ����� 20������ 64λ Intel������  
cmake version 3.13.4  
g++ (Uos 8.3.0.3-3+rebuild) 8.3.0  
git version 2.20.1  

## ���߰�װ
sudo apt-get install cmake  
sudo apt-get install g++  
sudo apt-get install git  

## ��������
sudo apt-get install build-essential git-core cmake libssl-dev libx11-dev libxext-dev libxinerama-dev libxcursor-dev libxdamage-dev libxv-dev libxkbfile-dev libasound2-dev libcups2-dev libxml2 libxml2-dev libxrandr-dev libavutil-dev libavcodec-dev libcunit1-dev libdirectfb-dev xmlto doxygen libxtst-dev uuid-dev libudev-dev  libusb-1.0 libdbus-glib-1-dev  
���ϰ�װ����������Щ����Ŀ�����Ϊ�����ز���������������װʧ�ܣ�������Щ���������Էֵ�����װ��

## ����rdp
git clone https://github.com/StrokeAce/YouboxRdp.git  
tar cvfz ./YouboxRdp.tar.gz ./YouboxRdp/  
cd YouboxRdp  
vi ./channels/urbdrc/ChannelOptions.cmake  
�� set(OPTION_CLIENT_DEFAULT OFF) ��Ϊ set(OPTION_CLIENT_DEFAULT ON)  
mkdir build  
cd build  
cmake ..  
make  
make DESTDIR=/opt/YouboxRDP install  
���installҲ�ɲ�ָ����װĿ¼

# Run
xfreerdp /u:15229349746 /p:349746 /w:1366 /h:768 /v:61.184.241.30:25788 /d:src /cert-ignore -sec-nla  
/u:�˺�  
/p:����  
/v:Զ�̵�ַ  
/d:����  
