# internet

A类网络的IP地址范围为：1.0.0.1－126.255.255.254；  

B类网络的IP地址范围为：128.1.0.1－191.255.255.254；  

C类网络的IP地址范围为：192.0.1.1－223.255.255.254  

具体解释： 

1．A类IP地址  

一个A类IP地址由1字节（每个字节是8位）的网络地址和3个字节主机地址组成，网络地址的最高位必须是“0”,即第一段数字范围为1～126。每个A类地址可连接16387064台主机，Internet有126个A类地址。  

2．B类IP地址  

一个B类IP地址由2个字节的网络地址和2个字节的主机地址组成，网络地址的最高位必须是“10”，即第一段数字范围为128～191。每个B类地址可连接64516台主机，Internet有16256个B类地址。  

3．C类IP地址  

一个C类地址是由3个字节的网络地址和1个字节的主机地址组成，网络地址的最高位必须是“110”，即第一段数字范围为192～223。每个C类地址可连接254台主机，Internet有2054512个C类地址。



子网掩码为 1 的部分表示网络号，子网掩码为 0 的部分表示主机号

IP 地址的主机号
全 0:表示整个子网
10.11.12.0/24

全 1:表示向子网上所有设备发送包，即“广播”
10.11.12.255/24

应用程序是通过“描述符”这一类似号码牌的东西来识别套接字的。

准确地说，IP 地址不是分配给每一台设备的，而是分配给设备中安装的网 络硬件的。因此，如果一台设备中安装了多个网络硬件，那么就会有多个 IP 地址。

IP 头部的“接收方 IP 地址”填写通信对象的 IP 地址。
发送方 IP 地址需要判断发送所使用的网卡，并填写该网卡的 IP 地址。

MTU:一个网络包的最大长度，以太网中一般为 1500 字节。 MSS:除去头部之后，一个网络包所能容纳的 TCP 数据的最大 长度。

描述符:应用程序用来识别套接字的机制
IP 地址和端口号:客户端和服务器之间用来识别对方套接字的机制


IP 模块负责添加如下两个头部。
(1) MAC 头部:以太网用的头部，包含 MAC 地址 (2) IP 头部:IP 用的头部，包含 IP 地址


IP 地址实际上并不是分配给计算机的，而是分配给 网卡的，因此当计算机上存在多块网卡时，每一块网卡都会有自己的 IP 地 址

路由表：
向Destination发包需要通过Gateway

IP 模块根据路由表 Gateway 栏的内容判断应该把包发送给谁。
