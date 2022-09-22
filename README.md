# PortScan 快速端口扫描器

一款运用`C++ Boost`准标准库开发的基于异步前摄器模型快速端口扫描器，该端口扫描器的优点是运用了异步扫描机制，扫描效率更高，同时支持批量验证一个网段内特定端口的开放情况。

 - 扫描特定主机`1-65534`全端口
```C
PortScan.exe --address 192.168.1.1 --type all
```

 - 扫描整个C段特定端口
 ```C
 PortScan.exe --c_address 192.168.1.1/10 --set_port 22,25
 ```
 
 - 指定扫描特定端口
 ```C
 PortScan.exe --address 192.168.1.1 --set_port 22,25,135,139
```
