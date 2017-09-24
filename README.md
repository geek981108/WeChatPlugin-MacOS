

![WeChat MenuBar](http://upload-images.jianshu.io/upload_images/8056623-d3c3657b8a37effa.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
---
主要实现 mac OS 版微信的消息防撤回与自动回复<的功能

---

### 更新日志
[添加全局毛玻璃效果&修改状态栏图标&去除“TK”]

---

### 功能
- 消息自动回复
- 消息防撤回
- 远程控制
- 微信多开
- 第二次登录免认证


远程控制：

-  屏幕保护
-  清空废纸篓
-  锁屏、休眠、关机、重启
- 退出QQ、WeChat、Chrome、Safari、所有程序
- 网易云音乐(播放、暂停、下一首、上一首、喜欢、取消喜欢)

**若想使用远程控制网易云音乐，请在“系统偏好设置 ==> 安全性与隐私 ==> 隐私 ==> 辅助功能”中添加微信**

---


### Demo 演示

* 消息防撤回


![防撤回测试.gif](http://upload-images.jianshu.io/upload_images/8056623-27789bcd4ef0a275.gif?imageMogr2/auto-orient/strip)
* 自动回复

![自动回复测试.gif](http://upload-images.jianshu.io/upload_images/8056623-e11e069da8dfe84a.gif?imageMogr2/auto-orient/strip)

* 微信多开

![微信多开.gif](http://upload-images.jianshu.io/upload_images/8056623-b1460bd58923b052.gif?imageMogr2/auto-orient/strip)

* 远程控制 (测试关闭Chrome、QQ、开启屏幕保护)
![远程控制.gif](http://upload-images.jianshu.io/upload_images/965383-0cf50d9b22b02f2f.gif?imageMogr2/auto-orient/strip)

* 免认证 & 置底
![免认证&置底](http://upload-images.jianshu.io/upload_images/965383-cc656af55cc2d2f6.gif?imageMogr2/auto-orient/strip)

---
### 安装

~~第一次安装需要输入密码，仅是为了获取写入微信文件夹的权限~~

**0. 懒癌版安装(适合非程序猿)**

打开`应用程序-实用工具-Terminal(终端)`，执行以下命令并根据提示输入密码即可。

`cd ~/Downloads && git clone https://github.com/geek981108/WeChatPlugin-MacOS.git && ./WeChatPlugin-MacOS/Other/Install.sh`

**1. 普通安装**

* 下载WeChatPlugin，用 Termimal 打开项目当前目录，执行 `./Other/Install.sh`即可。


**2. 若想修改源码&重编译**

* 先更改微信的 owner 以获取写入微信文件夹的权限，否则会出现类似**Permission denied**的错误。

`sudo chown -R $(whoami) /Applications/WeChat.app`

![Permission denied.png](http://upload-images.jianshu.io/upload_images/965383-11e4480553ba086e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* 下载 WeChatPlugin, 用Xcode打开，先进行 Build (`command + B`)，之后 Run (`command + R`)即可启动微信，此时插件注入完成。

* 若 Error，提示找不到 Framework，先进行 Build。

**3. 安装完成**

* 登录微信，在**菜单栏**中看到**🌚**即安装成功。

![微信助手.png](http://upload-images.jianshu.io/upload_images/8056623-ffc96e51b1a3a4df.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

---

### 使用

* 消息防撤回：点击`开启消息防撤回`或者快捷键`command + t`,即可开启、关闭。
* 自动回复：点击`开启自动回复`或者快捷键`conmand + k`，将弹出自动回复设置的窗口，点击红色箭头的按钮设置开关。

>若关键字为 `*`，则任何信息都回复；
>若关键字为`x|y`,则 x 和 y 都回复；
>若关键字**或者**自动回复为空，则不开启该条自动回复。
>若开启正则，请确认正则表达式书写正确，[在线正则表达式测试](http://tool.oschina.net/regex/)

![自动回复设置.png](http://upload-images.jianshu.io/upload_images/965383-5aa2fd8fadc545c4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


* 微信多开：点击`登录新微信`或者快捷键`command + shift + n`,即可多开微信。

* 远程控制：点击`远程控制 Mac OS`或者快捷键`command + shift + c`,即可打开控制窗口。


![远程控制.png](http://upload-images.jianshu.io/upload_images/8056623-5497692c82a1268e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

①为选择是否开启远程控制此功能。

②为能够触发远程控制的消息内容(仅向自己发送账号有效)。

---

### 卸载

在`Terminal`(终端)打开该项目，运行 `./Other/Uninstall.sh` 即可

---

### Other

若有其他好的想法欢迎 Issue me

---

---
