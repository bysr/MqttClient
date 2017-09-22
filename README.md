# [MqttClient](http://blog.csdn.net/qq_17250009/article/details/52774472)

> # 搭建服务器
 1. [下载](http://activemq.apache.org/apollo/download.html)Apollo服务器，选择windows平台下的服务器，[github地址](https://github.com/bysr/MqttClient/blob/master/apache-apollo-1.7.1-windows-distro.zip)
 2. dos命令进入解压后的bin目录
 3. 创建服务器，命令：*apollo create mybroker*(服务器名称)，bin目录下生成mybroker文件夹,文件夹下*etc\apollo.xml*文件下是配置服务器信息的文件。*etc\users.properties*文件包含连接MQTT服务器时用到的用户名和密码，默认为admin=password，即账号为admin，密码为password，可自行更改
 4. 进入XXX/bin目录，输入*apollo-broker.cmd run*开启服务器，看到如下界面代表搭建完成
 5.浏览器输入*http://127.0.0.1:61680/* 查看是否安装成功


> # Android客户端说明
 - topic：中文意思是“话题”。在MQTT中订阅了(subscribe)同一话题（topic）的客户端会同时收到消息推送。直接实现了“群聊”功能。
 - clientId：客户身份唯一标识。
 - qos：服务质量。
 - retained：要保留最后的断开连接信息。
 - MqttAndroidClient#subscribe()：订阅某个话题。
 - MqttAndroidClient#publish()： 向某个话题发送消息，之后服务器会推送给所有订阅了此话题的客户。
 - userName：连接到MQTT服务器的用户名。
 - passWord ：连接到MQTT服务器的密码。
