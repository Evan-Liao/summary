###《深入浅出Node.js》学习笔记

最近闲来没事，粗略阅读了一下这本书，受益匪浅，于是简单做下笔记，加深理解。

section 1 简介

简单介绍了Node的前世今生，Node的出现顺应了时代的发展需求。

section 2 模块机制

在Node出现之前，JavaScript只能通过script标签引入页面的，相对于其他语言的引入模块机制，这时候Javascript的地位
就可想而知了，所以就引入了模块的概念，就是Common.js。主要涉及三个概念：定义模块，引入模块，解释模块。

在这里，深入了解到调用JavaScript代码，背后究竟经历了什么。底层C++是难以li jie


section 3 异步I/O

section 7 网络编程

首先介绍了TCP，如何创建TCP服务以及一些基本概念，TCP属于传输层协议（OSI模型：物理层，链路层，网络层，传输层，会话层，表示层，应用层）,
服务端与客户端是通过套字节的方式建立连接，在此之前会发生三次握手，确定连接。在服务端，套字节是一个可读写的Stream流，因此可以进行管道操作（pipe）,
此时此刻，我联想起了gulp的工作模式。

接下来介绍UDP。UDP也属于传输层协议，又称数据包传输协议。与TCP最大但不同，UDP不是面向连接的。在TCP通过套字节完成连接后，意味所有会话已经完成，客户端如果要与另一个TCP服务进行通讯，则要建立新的套字节进行连接。但在UDP服务中，一个套字节可以与多个UDP服务通讯，提供面向事务的简单信息传输服务，在网络较差的情况下，存在掉包现象，但适用于传输视频，音频等场景，因为省去了连接，相对比较灵活。

