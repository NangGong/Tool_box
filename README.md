## 一个基于[ChatGPT-on-Wechat](https://github.com/zhayujie/chatgpt-on-wechat)项目的简单插件，直接调用一些实用的api接口！

基于Apilot插件新增了点内容

增加了调用第三方SD绘画

以及增加了随机头像，职场人日历的接口

如果使用SD需要配合PHP网站使用 [源码这里](https://github.com/NangGong/SD-ON-PHP)！

<img src="img/SD.png" width="600" >

### 安装

使用管理员口令在线安装即可，参考这里去如何[认证管理员](https://www.wangpc.cc/aigc/chatgpt-on-wechat_plugin/)！

```
#installp https://github.com/NangGong/ApilotSD.git
```

安装成功后，根据提示使用`#scanp`命令来扫描新插件，再使用`#enablep Apilot`开启插件，参考下图

<img src="img/安装.png" width="200" >

### 配置
直接安装不配置也可以使用一部分接口，部分接口(快递、天气)需要配置alapi的token。

* 服务器部署：复制插件目录的`config.json.template`文件并重命名为`config.json`，

  * `alapi_token`：填入申请的alapi token。

  * `morning_news_text_enabled`：默认false，发送早报图片；true，发送文字版早报。

* docker部署：参考项目docker部署的[插件使用](https://github.com/zhayujie/chatgpt-on-wechat#3-%E6%8F%92%E4%BB%B6%E4%BD%BF%E7%94%A8)，在挂载的config.json配置文件内增加`apilot`插件的配置参数，如下图，每次重启项目，需要使用 `#installp` 指令重新安装

  <img src="img/docker新参数.png" width="300" >

### Token申请

* `alapi_token`申请点击这里[alapi](https://admin.alapi.cn/account/center)

### 使用
* 对话框发送“早报”、“摸鱼”、"微博热搜（已更新为"微博热榜）"、”任意星座名称”可以直接返回对应的内容！

<img src="img/早报.png" width="600" >

<img src="img/摸鱼.png" width="600" >

<img src="img/星座.png" width="600" >

<img src="img/微博热搜.png" width="600" >



* 快递查询格式：快递+快递编号。如：快递YT2505082504474，如下图!


<img src="img/快递.png" width="600" style="display: block; margin: auto;" />



* 天气查询格式：城市+天气。如：成都天气。（支持3400+城市天气，输入不正确或者查询失败返回北京天气）

<img src="img/天气.png" width="600" style="display: block; margin: auto;" />		

* 热榜查询。支持:<微博/虎扑/知乎/哔哩哔哩/36氪/抖音/少数派/IT最新/IT科技>

<img src="img/热榜.png" width="600" >

