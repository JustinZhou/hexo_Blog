---
title: EdgeCast FTP Upload文件size变小问题的解决
date: 2016-08-13 16:38:58
tags:
---
最近在做EdgeCast CDN的评估，包括file的upload以及purge功能。因为之前有已经实现的ftp的组件，并且在实际生产中用于Akamai CDN的文件上传，未出现什么问题。然而，应用这个组件上传文件到edgecast的ftp上时发现文件竟然变小了！
起初我怀疑是edgecast ftp的问题，于是我就试着用现有的ftp软件8uftp去上传，发现不存在文件变小的问题。那么可能是我们代码的问题，可是奇怪的是为什么对于akamai的ftp就没有问题呢。此时我想到了用wireshark来捕捉ftp网络数据。
![](https://github.com/JustinZhou/images/raw/master/image1-1.jpg)
