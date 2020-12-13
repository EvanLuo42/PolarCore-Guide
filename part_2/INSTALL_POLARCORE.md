# 安装部署PolarCore

## 第一步：

前往[PolarCore项目地址](https://github.com/saltedfishclub/PolarCore)在Github Action中下载最新的构建版本，或在[本站](https://downloads.phakel.cn/Core-4.8.0-all.jar)下载。(本站使用2020/12/12的构建版本)

## 第二步：

将Core-x.x.x-all.jar放置在一个文件夹中，新建bat文件，用记事本写入如下内容：
```shell
java -jar Core-4.8.0-all.jar  //x.x.x请根据版本号填写
timeout /t 10 /nobreak > nul //这是为了在停止后可以看见命令行输出
```

## 第三步：

命令行输出如下：

```shell
12:45:07 [37m[main][0;39m [34mINFO [0;39m - PolarCore V4.8.0 starting..
12:45:07 [37m[main][0;39m [34mINFO [0;39m - Java Version: 11.0.9+7-LTS
12:45:07 [37m[main][0;39m [34mINFO [0;39m - Loading Modules..
12:45:07 [37m[main][0;39m [34mINFO [0;39m - Go to edit your config first :D
12:45:07 [37m[Thread-0][0;39m [34mINFO [0;39m - Interrupt signal received!
12:45:07 [37m[Thread-0][0;39m [1;31mERROR[0;39m - Core is null! Maybe polar didn't initialize completed or something wrong?
```

出现以上现象是正常反应，只需重新双击bat启动，即可出现以下：

```shell
12:47:04 [37m[main][0;39m [34mINFO [0;39m - PolarCore V4.8.0 starting..
12:47:04 [37m[main][0;39m [34mINFO [0;39m - Java Version: 11.0.9+7-LTS
12:47:04 [37m[main][0;39m [34mINFO [0;39m - Loading Modules..
12:47:04 [37m[main][0;39m [34mINFO [0;39m - Loading Database..
12:47:04 [37m[main][0;39m [34mINFO [0;39m - HikariPool-1 - Starting...
12:47:04 [37m[main][0;39m [34mINFO [0;39m - HikariPool-1 - Start completed.
12:47:04 [37m[main][0;39m [34mINFO [0;39m - Modules Loaded.
```

到这里，PolarCore的部署部分就结束了，下一章将教学如何与QQ平台连接。