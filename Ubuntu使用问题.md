###### 1. Ubuntu 开机紫屏无法进入图形界面

1. 进入Ubuntu引导界面，选择`ubuntu Advance`，第一行的内核即为崩溃的内核。
  
2. 更换内核直至可以进入图形界面，在终端输入`uname -a`查看当前内核版本。
  
3. 在终端输入`dpkg --list | grep linux-image`查看所有内核版本。
  
4. 在终端输入`sudo dpkg --configure -a`尝试修复内核。
  
5. 如果在修复过程中仍然报错，则可以卸载该内核。
  
6. 在终端输入`sudo apt-get remove --purge linux-image-unsigned-4.15.0-142-generic`卸载崩溃的内核。
  

&emsp;
