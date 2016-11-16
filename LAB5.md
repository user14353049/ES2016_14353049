#配置ROS
###ROS:
* Robot operating system(ROS) 是一个构建机器人及应用的操作系统，采用 BSD 许可协议。ROS 的主要目标是为机器人研究和开发提供代码复用的支持。ROS 提供了 C++ 和 Python 两种主要的编程接口，提供了类似 Debian 的包管理系统，开发者能方便的开发、安装、管理应用包。\

##实验过程

1. 配置Ubuntu要求允许接受"restricted," "universe," and "multiverse."的软件源,默认配置就是这个，可以不用自行配置。

2. 设置编辑源列表:
	sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'


3. 设置密钥:
	sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116


 4. 安装

* 更新Debian软件包索引是最新的
	
	sudo apt-get update

* 安装Desktop-Full

	sudo apt-get install ros-jade-desktop-full

* 下载Individual Package

	sudo apt-get install ros-jade-PACKAGE
	sudo apt-get install ros-jade-slam-gmapping

* 寻找可用的包
	
	apt-cache search ros-jade

* 初始化rosdep

	sudo rosdep init
	rosdep update

5.  设置环境

	添加ROS的环境变量,这样,当你打开你新的shell时,你的bash回话中会自动添加环境变量。
	echo "source /opt/ros/jade/setup.bash" >> ~/.bashrc
	source ~/.bashrc

6. 安装rosinstall

	sudo apt-get install python-rosinstall





