# MinecraftPE-Ping

---

通过UDP协议获取MCPE的服务器状态    
此接口用PHP搭建,以 [PluginsKers][1] 大大的[Motd_For_Minecraft][2] 项目精简而来,保留了原来的功能,废除了非必要的连接数据库部分的代码,你的服务端只需搭建了php环境即可使用(请使用php5以上版本)

测试接口地址：http://abcd2586.w3.luyouxia.net/api/mcpe/?ip=www.the-ink-man.xyz&port=19132
请求方式GET/POST

参数|示例|描述
-|-|-
ip|www.the-ink-man.xyz|服务器IP地址
port|19132|服务器端口

返回JSON数据

参数|示例|描述
-|-|-
status|online|服务器唯一状态识别
ip|www.the-ink-man.xyz|返回查询IP
port|19132|返回查询端口
motd|富强民主文明和谐自由平等公正法治爱国敬业诚信友善|服务器广播内容Motd
agreement|407|协议版本
version|1.16.0|客户端版本
online|0|服务器在线人数
max|65|服务器人数上限
dbname|PocketMine-MP|服务器房间名称
gamemode|Survival|游戏模式
delay|444|连接服务器延迟(ms)

代码中设置的超时时间为5秒
ip 和 port 是必填参数,否则直接返回offline


  [1]: https://github.com/PluginsKers
  [2]: https://github.com/PluginsKers/Motd_For_Minecraft