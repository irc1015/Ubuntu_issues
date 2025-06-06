#### 1. Ubuntu 开机紫屏无法进入图形界面

1. 进入Ubuntu引导界面，选择`ubuntu Advance`，第一行的内核即为崩溃的内核。
  
2. 更换内核直至可以进入图形界面，在终端输入`uname -a`查看当前内核版本。
  
3. 在终端输入`dpkg --list | grep linux-image`查看所有内核版本。
  
4. 在终端输入`sudo dpkg --configure -a`尝试修复内核。
  
5. 如果在修复过程中仍然报错，则可以卸载该内核。
  
6. 在终端输入`sudo apt-get remove --purge linux-image-unsigned-4.15.0-142-generic`卸载崩溃的内核。
---
#### 2. Ubuntu 无法使用拼音输入法

1. 在 **设置** 中的 **键盘** 一栏中移除 **中文（智能拼音）**

2. 在 **终端** 中输入 `sudo apt-get install ibus-pinyin` 重新安装拼音输入法

3. 在 **设置** 中的 **键盘** 一栏中添加关于中文输入法的 **输入源**

---

#### 3. 安装 deb 安装包

``` bash
sudo apt install ./文件名.deb
```



