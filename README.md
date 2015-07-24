# managerServer
批量服务器管理程序，fun.py是主程序，fun是function的简写。

fun.py：功能程序，支持批量分发、接收文件、允许批量分发执行远程命令、服务器分组管理、主机和组的添加

menu.py：菜单表格

host_info.py: python连接mysql数据库程序

manager.sql：数据库表结构，里面有两个表，分别是host和groups表，直接导入即可

conn_host.py：多线程批量下发文件和执行命令，使用了pexpect,pxssh和threading模块





主菜单界面：
root@mico-KVM:~/python/github/python/test/socket# python fun.py
Menu info:

	1.	Choose the host
	2.	Choose the group
	3.	View all hosts
	4.	Added(Delete) info(Host or group)
	5.	Exit

Please input your choose: 




二级部分菜单界面：
Menu info:   ##添加删除主机和组功能菜单

	1.	Add host
	2.	Add group
	3.	Del host
	4.	Del group
	5.	Host added to group
	6.	Exit

Please input your choose: 

Menu info:    ##批量下发命令或下发文件菜单

	1.	Execute commands
	2.	Copy Files
	3.	Exit

Please input your choose: 




部分演示功能：
Please input you want to choose or input 'quit' will exit: test     ##批量执行命令
Menu info:

	1.	Execute commands
	2.	Copy Files
	3.	Exit

Please input your choose: 1
Please input you need to run command or input 'quit' will exit: ifconfig eth1
Fri Jul 24 09:48:57 2015
current has 3 threads

-------------------------------test_member----------------------------------

ifconfig eth1
eth1      Link encap:Ethernet  HWaddr 52:54:00:68:7C:19  
          inet addr:172.16.20.53  Bcast:172.16.20.255  Mask:255.255.255.0
          inet6 addr: fe80::5054:ff:fe68:7c19/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:17497021 errors:0 dropped:0 overruns:0 frame:0
          TX packets:1082960 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000 
          RX bytes:1945818951 (1.8 GiB)  TX bytes:643548861 (613.7 MiB)


Fri Jul 24 09:48:59 2015

-------------------------------test_pay----------------------------------

ifconfig eth1
eth1      Link encap:Ethernet  HWaddr 52:54:00:68:7C:55  
          inet addr:172.16.20.55  Bcast:172.16.20.255  Mask:255.255.255.0
          inet6 addr: fe80::5054:ff:fe68:7c55/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:39101264 errors:0 dropped:0 overruns:0 frame:0
          TX packets:19874409 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000 
          RX bytes:4554745204 (4.2 GiB)  TX bytes:1943685978 (1.8 GiB)


		  
Menu info:			###批量下发文件

	1.	Execute commands
	2.	Copy Files
	3.	Exit

Please input your choose: 2
Please input you need to copy of the file name or input 'quit' will exit: tab.py
Please input you need to save path or input 'quit' will exit: /tmp
Fri Jul 24 09:50:18 2015
current has 3 threads

-------------------------------test_member----------------------------------
 
tab.py                                        100%  417     0.4KB/s   00:00    

Fri Jul 24 09:50:18 2015

-------------------------------test_pay----------------------------------
 
tab.py                                        100%  417     0.4KB/s   00:00    

Fri Jul 24 09:50:18 2015

-------------------------------test_www----------------------------------
 
tab.py                                        100%  417     0.4KB/s   00:00    

Fri Jul 24 09:50:19 2015


其它部分添加删除主机和组功能不在演示。






联系我（mico）
Email:zihepeng@126.com
