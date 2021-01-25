ubuntu_tips

1. 运行32位系统

   

```
确认系统架构
dpkg --print-architecture
1
确认输出为amd64，即系统为64位

确认多架构支持功能
dpkg --print-foreign-architectures
1
确认输出为i386

sudo dpkg --add-architecture i386
sudo apt-get update
1
2
安装32位库
sudo apt-get dist-upgrade                 	 #更新所有软件，可选
sudo apt-get install lib32z1 lib32ncurses5 
sudo apt-get install gcc-multilib g++-multilib 

#安装gcc multilab
```

2. win10下  linux 64位无法运行32位

主要原因是：子系统不支持原生linux文件头。

需要添加原生linux形式文件头支持：

```bash
sudo apt update
sudo apt install qemu-user-static
sudo update-binfmts --install i386 /usr/bin/qemu-i386-static --magic '\x7fELF\x01\x01\x01\x03\x00\x00\x00\x00\x00\x00\x00\x00\x03\x00\x03\x00\x01\x00\x00\x00' --mask '\xff\xff\xff\xff\xff\xff\xff\xfc\xff\xff\xff\xff\xff\xff\xff\xff\xf8\xff\xff\xff\xff\xff\xff\xff'
```

> https://blog.csdn.net/fangye945a/article/details/105777266