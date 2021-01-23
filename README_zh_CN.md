# Telegraque
[中文版本](README_zh_CN.md) | [English](README.md)  
在QQ和Telegram之间同步消息。

# 简介
一个可扩展的在QQ、Telegram或其它平台之间同步消息的项目。

# 为什么会有这个项目
有太多的聊天软件了，每天看这些聊天软件上的消息就会占用大量时间。
  
# 设计
项目包含三个主要部分：主动部分（比如Telegram，可以发起一个聊天会话或者做一些其它主动的事情），中间处理部分（或者称为中间件，在两个部分之间同步消息），被动部分（比如使用Marai制作的QQ机器人，
发送所有其收到的消息）。  
考虑到这几个部分都会同时收发消息，每个部分都将会被设计成可以通用于主动或者被动模式。

# 如何使用
您可以直接从github release下载或者运行
```shell
git clone https://github.com/ForeverOpp/Telegraque.git
```
接着按照您想要的方式配置`config.example.yaml`，并重命名为`config.yaml`。  
要了解如何配置，请参阅[如何正确配置](docs/config.md)。  
如果您使用了某些特定插件或者主被动部分，比如QQ，您还需要安装一些额外的东西。下面的表格列出了一些支持的插件和他们的文档。  
  
|   插件名称 |   文档链接                                |
|   :----:  |   :----:                              |
|   QQ      |   [QQ](docs/plugins/QQ.md)            |
|   Telegram|   [Telegram](docs/plugins/Telegram.md)|
  
您当然也可以通过参阅[中间件解释](docs/mid-ware.md)来开发自己的主被动部分（插件）。  
当您完成上述步骤，您可以运行  
```shell
go telegraque.go
```
而且，您也可以使用`telegraqued.go`来把它作为一个服务使用。  
  
# 许可与注意
本工具仅作为学习交流使用，我们不保证任何由不当使用此工具导致的后果。  
有关协议，请参阅[这里](LICENSE)。

