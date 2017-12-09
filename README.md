Copyright (C) 2017 The LineageOS Project

Device configuration for Nubia Z11 

qq群648044729

开始编译：

1.设置编译环境

source build/envsetup.sh

2.设置加快编译速度

 export USE_CCACHE=1
 
3.加入root

export WITH_SU=true

4.设置缓存

 ~/aokp/prebuilts/misc/linux-x86/ccache/ccache -M 80G


 export JACK_SERVER_VM_ARGUMENTS="-Dfile.encoding=UTF-8 -XX:+TieredCompilation -Xmx16000m"（本人内存8g，所以这里允许内存填8192M）

4.开安装jack，

进prebuilts/sdk/tools文件夹打开终端，

./jack-admin install-server jack-launcher.jar jack-server-4.8.ALPHA.jar

5.并且开启jack服务。

如何编译到一半失败,请关闭j开启jack或者,手动杀死java服务.不然的话16g内存也不够用.

./prebuilts/sdk/tools/jack-admin kill-server

./prebuilts/sdk/tools/jack-admin start-server

6.编译开始

breakfast  nx531j

make -j8

注意：如何编译到一半失败,请关闭j开启jack或者,手动杀死java服务.不然的话16g内存也不够用.

./prebuilts/sdk/tools/jack-admin kill-server

./prebuilts/sdk/tools/jack-admin start-server

7.打包

mka bacon



## Device picture

![Nubia Z11](http://static.nubia.cn/product/z11/images/gallery/7.jpg "Nubia Z11 Standard Edition")
