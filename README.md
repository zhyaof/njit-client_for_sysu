njit-client_for_sysu
-----
njit-client_for_sysu旨在为Linux或Openwrt环境提供H3C 802.1X认证客户端。
简介
-----
本项目解决了SYSU使用Linux或Openwrt登录认证问题。<br/>经测试SYSU完美兼容，兼容明文传输密码以及md5密码加密。 <br/>兼容iNode PC V3.6(E6208)、iNode PC V5.0(E0101)和iNode PC V5.1。
安装
-----
从源码安装。先安装对应开发包。<br/>
对应Ubuntu/Debian的是：<br/>
sudo apt-get install libpcap-dev libssl-dev<br/>
对应Fedora/Redhat的是：<br/>
yum install libpcap-devel openssl-devel <br/>
从源码包开始编译客户端的命令为：<br/>
tar xzf njit8021xlient-1.1.tar.gz<br/>
cd njit8021xlient-1.1<br/>
./configure make <br/>
安装：<br/>
make install<br/>
注1： 默认安装至/usr/local目录，需要root管理员权限。 
使用方法
-----
通过命令行切换为root并运行njit-client程序：<br/>
Ubuntu下命令格式为： <br/>
sudo njit-client user_name password <br/> 
RedHat/Fedora下命令格式为：<br/>
su -c "njit-client user_name password"<br/>
说明
-----
本项目基于刘群的njit-client开发，项目地址：https://github.com/liuqun/njit8021xclient 感谢@狼王弱爆了 为我们改写了其md5。md5参考自Maple的YaH3C。