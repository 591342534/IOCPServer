# IOCPServer
A IOCP Server Class on Windows!
 
 
本类配套文章：http://www.cnblogs.com/tanguoying/p/8439701.html


一个基于完成端口网络服务类，自带缓存池和心跳包监测！

* 这个类IOCP是本代码的核心类，用于说明WinSock服务器端编程模型中的完成端口(IOCP)的使用方法

* 其中的IOContext类是封装了用于每一个重叠操作的参数

* 具体说明了服务器端建立完成端口、建立工作者线程、投递Recv请求、投递Accept请求的方法，所有的客户端连入的Socket都需要绑定到IOCP上，所有从客户端发来的数据，都会调用回调函数。

* 用法：派生一个子类，重载回调函数

Author: TTGuoying
Date: 2018/02/07 16:22
开发工具 ：VS2017

 -----------------------------------------------------------------

* 增加对X64平台支持

* 修改退出信号类型,用以排除在x64平台编译警告

* 补齐PostSend()

* 修复WorkerThreadProc()线程过早释放主进程的IOPC管理类造成stop重复释放bug.

regenerator:LouiWang
Date: 2020/07/24
开发工具 : vs 2017
