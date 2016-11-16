#LAB2 DOL实例分析&编程

##实验任务

* 修改example2，让3个square模块变成2个, tips:修改xml的iterator 

*  修改example1，使其输出3次方数，tips:修改square.c 

提示：修改代码之后要重新编译、运行（sudo ant –f runexample.xml –Dnumber=XXX）XXX是 运行example的号码，比如上面是2和1.

##实验过程

###1.修改example2，让3个square模块变成2个, tips:修改xml的iterator 

* example2中square模块在example2.xml文件中进行修改：
* 模块对应变量value，所以将value = 3改为value = 2 :

 ![example2.xml](https://ooo.0o0.ooo/2016/11/11/5826073f5d786.png)
####更改后成功结果：
![example](https://ooo.0o0.ooo/2016/11/11/58260832d9721.png)
![example](https://ooo.0o0.ooo/2016/11/11/582608330339b.png)


###2.修改example1，使其输出3次方数，tips:修改square.c 
* 更改square.c中的运算部分，如下图：

 ![example1](https://ooo.0o0.ooo/2016/11/11/5826064dc0b9e.png)
####更改后成功结果：
![example1](https://ooo.0o0.ooo/2016/11/11/582608330339b.png)
![example1](https://ooo.0o0.ooo/2016/11/11/58260832d9721.png)
##实验感想

* 更改dol实例了解了各个文件功能;
* src文件夹：各进程（生产者，消费者，处理模块）的功能定义;
* example1.xml：系统架构（即模块连接方式定义）;
* 学会了通过vim对文档进行更改;