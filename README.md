gcc-for-android
===============
最简单的方法：

         首先下载个GCC Plugin for C4droid

         官方下载地址：https://market.android.com/details?id=com.n0n3m4.gcc4droid

         或者这个地址，感谢Oxt提供的（ps：网上搜的）：http://115.com/file/bhtwhm5k#                com.n0n3m4.gcc4droid-1.apk

         我自己上传的是这个（gcc.zip，也就是拿出来的文件）:http://115.com/file/belmf820#

         然后，在WIN下可以用解压的方法提取出里面的gcc.zip。因为GCC是免费的，而且GCC的条款的规定可以让我们合法利用这个。也就是说我们所做的并非是什么偷鸡摸狗之事。或者，在LINUX下直接打开文件，解压出来。方法是一样的，在MAC上也是如此。

[python] view plaincopyprint?
adb remount  
adb shell  
adb push gcc /sd-ext/home/gcc  
也就是将文件放到手机上的某个地方，因为将这个作为HOME目录的关系，所以也是这个作为gcc的目录。
然后，gcc/bin下的两个文件为gcc g++，比较方便
接着修改下home目录的.profile，添加上这么几行
[python] view plaincopyprint?
export GCCHOME="/sd-ext/home/gcc"                                                 
export GCCPATH=$GCCHOME/bin:$GCCHOME/arm-linux-androideabi/bin:$GCCHOME/libexec/  
export PATH=$PATH:$GCCHOME:$GCCPATH ］  
试着写个hello.c运行下。也就是传说中的android gcc，很帅吧



关于android bash的方法，自带的终端用的是sh不是bash，也因此我们可以用这个，比较吸引人。

           下载地址：http://115.com/file/belm038k#

           方法就是push到那些文件中，然后就OK了。


Android上使用python也是如此方法，除了在.profile上些许不同之外，都是将文件push到home目录就行了。

搜索sl4a,下载地址:code.google.com/p/android-scripting/


[python] view plaincopyprint?
export PYTHONHOME="/sd-ext/home/usr/python2.6"  
export PYTHONPATH=.:$PYTHONHOME:$PYTHONHOME/site-packages  
export PATH=$PATH:$PYTHONHOME:$PYTHONPATH  

