---
title: Screen的使用方法
date: 2021-08-06 16:36:27
tags: [Linux, 部署]
categories: 服务器
---
## 为什么要使用screen命令
VPS侦探在刚接触Linux时最怕的就是SSH远程登录Linux VPS编译安装程序时（比如安装lnmp）网络突然断开，或者其他情况导致不得不与远程SSH服务器链接断开，远程执行的命令也被迫停止，只能重新连接，重新运行。相信现在有些VPSer也遇到过这个问题，今天就给VPSer们介绍一款远程会话管理工具 - screen命令。
## 一、screen命令是什么？
Screen是一个可以在多个进程之间多路复用一个物理终端的全屏窗口管理器。Screen中有会话的概念，用户可以在一个screen会话中创建多个screen窗口，在每一个screen窗口中就像操作一个真实的telnet/SSH连接窗口那样。
## 二、如何安装screen命令？
除部分精简的系统或者定制的系统大部分都安装了screen命令，如果没有安装，CentOS系统可以执行：
``` bash
yum install screen
``` 
CentOS 8上移除了screen，需要安装epel后安装screen执行：
``` bash
yum install screen
``` 
Debian/Ubuntu系统执行：
``` bash
apt-get install screen
``` 
## 三、screen命令使用方法？
### 1、常用的使用方法
用来解决文章开始我们遇到的问题，比如在安装lnmp时。
#### 1.1 创建screen会话
screen创建一个名字为lnmp的会话。 VPS侦探 https://www.vpser.net/; 可以先执行：
``` bash
screen -S lnmp
```
#### 1.2 暂时离开，保留screen会话中的任务或程序

当需要临时离开时（会话中的程序不会关闭，仍在运行）可以用快捷键Ctrl+a d(即按住Ctrl，依次再按a,d)

#### 1.3 恢复screen会话

恢复到离开前创建的lnmp会话的工作界面,执行：
``` bash
aaaq lnmp 
```
如果忘记了,或者当时没有指定会话名,列出当前存在的会话列表,可以执行：
``` bash
screen -ls screen
```
11791.lnmp即为刚才的screen创建的lnmp会话，目前已经暂时退出了lnmp会话，所以状态为Detached，当使用
``` bash
screen -r lnmp
```
后状态就会变为Attached，11791是这个screen的会话的进程ID，恢复会话时也可以使用：
``` bash
screen -r 11791
```

#### 1.4 关闭screen的会话

执行：
``` bash
exit
```
会提示：[screen is terminating]，表示已经成功退出screen会话。VPS侦探 https://www.vpser.net/
#### 1.5 删除会话
``` bash
screen -S session_name -X quit
```
or
``` bash
screen -X -S 122128 quit
```
### 2、远程演示
首先演示者先在服务器上执行:
``` bash
screen -S test
```
创建一个screen会话，观众可以链接到远程服务器上执行:
``` bash
screen -x test
```
观众屏幕上就会出现和演示者同步。

### 3、常用快捷键

#### 3.1 在当前screen会话中创建窗口
Ctrl+a c

#### 3.2 窗口列表
Ctrl+a w

#### 3.3 下一个窗口
Ctrl+a n

#### 3.4 上一个窗口
Ctrl+a p

#### 3.5 在第0个窗口和第9个窗口之间切换
Ctrl+a 0-9
Ctrl+a 0-9
![添加微信](Server_Screen/WX_QR_code.png)
