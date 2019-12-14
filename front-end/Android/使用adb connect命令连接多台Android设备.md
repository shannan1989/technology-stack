除了使用USB方式连接Android设备外，还有一种方法是通过 adb connect 命令利用TCP/IP协议来连接Android设备。毕竟，PC端的USB口也是有限的。

## Step1：

设置手机和PC连接同一WIFI；

用USB连接手机与PC；

在终端输入：
```
adb tcpip 5555
```
解释：5555 端口是默认端口，也可以用其他端口。

## Step2：

断开手机与PC的USB连接，在终端输入：

adb connect IP:5555

比如这样：
```
adb connect 192.168.1.10:5555
```
终端会返回：connected to 192.168.1.10:5555

表示连接成功。

## Step3:

查看连接设备，在终端输入：
```
adb devices
```
可以看到，设备已连接。


当需要连接多台设备时，可重复上面的操作，但是端口号需要变一下。

需要注意的是，如果一台手机同时通过USB和tcpip连接到PC，adb devices会识别出2台设备，但其实是同一台手机的2种连接方式。

当不再需要设备连接时，利用 adb disconnect 命令来断开连接：
```
adb disconnect 192.168.1.10:5555
```
