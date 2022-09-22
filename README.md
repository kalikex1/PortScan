# PortScan 快速端口扫描器

<br>

<div align=center>

![logo](https://user-images.githubusercontent.com/52789403/191661175-453d2499-036c-434a-b548-0a38a3bbbfb7.png)

</div>

<br>

一款运用`C++ Boost`准标准库开发的基于异步前摄器模型快速端口扫描器，该端口扫描器的优点是运用了异步扫描机制，扫描效率更高，同时支持批量验证一个网段内特定端口的开放情况。

目前扫描器无壳无特征，不会被杀，且程序只有`327KB`适合远程传输以及横向渗透时收集端口信息。

 - 工具参数列表预览
```C
Shell > PortScan.exe
 ____            _     ____
|  _  ___  _ __| |_  / ___|  ___ __ _ _ __
| |_) / _ |  __| __| ___  / __/ _  |  _
|  __/ (_) | |  | |_   ___) | (_| (_| | | | |
|_|   ___/|_|   __| |____/ _____ _|_| |_|

 Usage: 异步端口扫描器
 Email: me@lyshark.com

 Options:
  -a [ --address ] arg   指定扫描地址 192.168.1.1
  -c [ --c_address ] arg 设置扫描C地址段 192.168.1.1/24
  -s [ --set_port ] arg  设置扫描端口 80,443,135,139
  -t [ --type ] arg      对特定主机 扫描 1-65535 全端口
  -h [ --help ]          帮助菜单
```

<br>

 - 扫描特定主机`1-65534`全端口开放情况
```C
PortScan.exe --address 192.168.1.1 --type all
```

 - 扫描特定地址段的特定端口开放情况
 ```C
 PortScan.exe --c_address 192.168.1.1/221 --set_port 22,25
 ```
 
 - 指定扫描特定主机的特定端口开放情况
 ```C
 PortScan.exe --address 192.168.1.1 --set_port 22,25,135,139
```
