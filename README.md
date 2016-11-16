#DOL开发配置实验
##Description
Distributed Operation Layer : 
The distributed operation layer (DOL) is a software development framework to program parallel applications. 
##Configure DOL
### Configure Environment
* $ sudo apt-get update
* $ sudo apt-get install ant
* $ sudo apt-get install openjdk-7-jdk
* $ sudo apt-get install unzip
###Configure DOL
####Download DOL

* sudo wget http://www.accellera.org/images/downloads/standards/systemc/systemc-2.3.1.tgz
* sudo wget http://www.tik.ee.ethz.ch/~shapes/downloads/dol_ethz.zip   


####Unzipfile

* $ sudo mkdir dol 
* $ sudo unzip dol_ethz.zip -d dol 
* $ sudo tar -zxvf systemc-2.3.1.tgz


####Compile Systemc

* $ cd systemc-2.3.1
* $ mkdir objdir 
* $ cd objdir
* $ ../configure CXX=g++ --disable-async-updates
* $ make install


####Compile DOL

进入刚刚dol的文件夹

* $ cd ../dol


修改build_zip.xml文件 找到下面这段话,就是说上面编译的systemc位置在哪里, 

编译dol

进入刚刚dol的文件夹


* $ cd ../dol


修改build_zip.xml文件 找到下面这段话,就是说上面编译的systemc位置在哪里, 

* <property name="systemc.inc" value="YYY/include"/>
* <property name="systemc.lib" value="YYY/lib-linux/libsystemc.a"/> 

把YYY改成上页pwd的结果(注意,对于 64位 系统的机器,lib-linux要改成lib-linux64)
然后是编译

* $ ant -f build_zip.xml all


成功会显示build successful
Run example1:

* $ cd dol/build/bin/main
* $ ant -f runexample.xml -Dnumber=1


把YYY改成上页pwd的结果(注意,对于 64位 系统的机器,lib-linux要改成lib-linux64)
然后是编译

* $ ant -f build_zip.xml all

成功会显示build successful
Run example1:

* $ cd dol/build/bin/main
* $ ant -f runexample.xml -Dnumber=1

成功配置后的图片：
![1](http://i1.piimg.com/4851/a3330204c955a6e1.png)

##Experimental experience
通过本次试验我学会了

* 在虚拟机上配置dol环境；
* Github仓库的建立；
*  Markdown的基本语法；


