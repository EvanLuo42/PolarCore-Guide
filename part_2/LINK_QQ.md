# 连接QQ平台

在关于PolarCore的介绍中已经提到了，想要将PolarCore应用在QQ平台上，需要借助①MiraiAdapter。所以需要将MiraiAdapter插件安装在PolarCore。

## 第一步：

你可以选择在[Adapter仓库](https://github.com/project-polar/MiraiAdapter)clone后编译。也可以选择在[本教程](https://downloads.phakel.cn/MiraiAdapter-1.0-SNAPSHOT-all.jar)下载。

## 第二步：

把下载到的jar文件丢入PolarCore根目录下的plugins文件夹，并重启PolarCore。应该会在插件配置文件夹中生成config.json，如下：

```json
{
  "baseUrl": "http://localhost:8080/",
  "QQ": 3325273573,
  "authKey": "AuthKey_HERE",
  "displayMessage": false,
  "autoCreateAccount": true,
  "autoAcceptFriendRequest": true,
  "autoAcceptGroupRequest": true
}
```

### 第三步：

本教程已经整合了一份Mirai懒人包，[点击](https://downloads.phakel.cn/Mirai.zip)下载。下载后双击bat，出现如下输出：

```shell
2020-12-13 13:01:54 I/main: Starting mirai-console...
2020-12-13 13:01:54 I/main: Backend: version 1.0-M4, built on 2020-09-13 02:19:35.
2020-12-13 13:01:54 I/main: Frontend Pure: version 1.0-M4, provided by Mamoe Technologies
2020-12-13 13:01:54 V/main: Loading configurations...
2020-12-13 13:01:55 V/main: Loading JVM plugins...
2020-12-13 13:01:55 I/plugin: Successfully loaded plugin MiraiApiHttp
2020-12-13 13:01:55 V/main: 0 external PluginLoader(s) found.
2020-12-13 13:01:55 V/main: 1 plugin(s) loaded.
2020-12-13 13:01:55 V/main: Loading PermissionService...
2020-12-13 13:01:55 V/main: Reloaded PermissionService settings.
2020-12-13 13:01:55 V/main: Loading built-in commands...
2020-12-13 13:01:55 V/main: Prepared built-in commands: help, login, permission, stop
2020-12-13 13:01:55 V/main: Enabling plugins...
2020-12-13 13:01:55 I/MiraiApiHttp: Starting Mirai HTTP Server in 0.0.0.0:8080
2020-12-13 13:01:55 W/MiraiApiHttp: USING INITIAL KEY, please edit the key
2020-12-13 13:01:55 I/MiraiApiHttp: Starting Mirai HTTP Server in 0.0.0.0:8080
2020-12-13 13:01:55 I/Mirai HTTP API: Http api server is running with authKey: INITKEYb373gYQ9
2020-12-13 13:01:55 I/MiraiApiHttp: 心跳模块启用状态: true
2020-12-13 13:01:55 I/MiraiApiHttp: 上报模块启用状态: true
2020-12-13 13:01:55 I/main: 1 plugin(s) enabled.
2020-12-13 13:01:55 I/main: mirai-console started successfully.
```

记下authKey。使用login QQ号 QQ密码登录你的QQ账号。

### 第四步：
将authKey填入刚刚生成的config.json，并填入你登入的QQ号，如下：

```json
{
  "baseUrl": "http://localhost:8080/",
  "QQ": xxxxxxxxx,
  "authKey": "INITKEYb373gYQ9",
  "displayMessage": false,
  "autoCreateAccount": true,
  "autoAcceptFriendRequest": true,
  "autoAcceptGroupRequest": true
}
```

然后重启PolarCore。

到了这里，配置就已经完成了，可以对机器人发送!p mirai image查看是否成功。如果不喜欢默认的!p前缀，可以修改PolarCore根目录config.json中的commandPrefix键。

*注释：①关于Mirai是什么，详见[Mirai仓库](https://github.com/mamoe/mirai)。