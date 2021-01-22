# Telegraque
[中文版本](README_zh_CN.md) | [English](README.md)  
Sync messages from QQ to Telegram.
  
# Introduction
An expandable sync program from QQ or other platforms to Telegram or other platforms.  

# Why doing this?
There are too many chat programs to use. We need to install them and check them for many times. For solving this messy problem,
Telegraque was created.
  
# Design
It contains 3 mainly part: Initiative Parts(like Telegram, can launch a chat session or do something initiative),
Mid-Processor(or Mid-ware, sync between two parts), Passive Parts(like QQ bot from Marai, send all messages to the mid-ware).
Considering that these parts will send and get messages at the same time,
each part will be designed to adapt for commonly use to be passive or initiative.

# How to use?
You can directly download from github release or run
```shell
git clone https://github.com/ForeverOpp/Telegraque.git
```
Then config the `config.example.yaml` as you want and rename it to `config.yaml`.  
To know how to config, see [How can I config it properly](docs/config.md).  
If you use some special plugins or parts like QQ, you need to install some extra things. Below is a table which list some
supported plugins and their docs.   
  
|   Plugins |   Docs                                |
|   :----:  |   :----:                              |
|   QQ      |   [QQ](docs/plugins/QQ.md)            |
|   Telegram|   [Telegram](docs/plugins/Telegram.md)|
  
You can also develop your own parts by reference [Mid-ware explanation](docs/mid-ware.md).  
When you finished them properly, you can simply use it by
```shell
go telegraque.go
```
Also, you can set it as service by using `telegraqued.go`.
  
# License and Notice
This tool is only for communication, so we DO NOT assume any consequences caused by improper use of this tool.  
See license [here](LICENSE).

