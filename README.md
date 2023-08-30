# ZTAS-MERCURY
这是[ZTAS](https://github.com/kaidunztas/ztas)平台的管理端，组织机构的管理员通过该程序注册组织机构的域，管理域内的用户，数据中心、数据中心内的Venus设备，IT服务，EWP管理,NSP管理、DNS管理等。

支持的操作系统：
* Linux：支持
* Windows: 支持
* Mac: 支持

# 下载和安装

## Linux
到[Linux](https://github.com/kaidunztas/ztas-mercury/tree/main/linux) 目录里下载ZIP包，存放于本地，解压即可。

## Windows
到[Windows](https://github.com/kaidunztas/ztas-mercury/tree/main/windows) 目录里下载ZIP包，存放于本地，解压即可。

## Mac
到[Mac](https://github.com/kaidunztas/ztas-mercury/tree/main/darwin) 目录里下载ZIP包，存放于本地，解压即可。

# 用户手册

## 启动

### Linux
1. 打开一个命令行窗口
2. 转到本程序的解压目录
3. 输入以下命令：.\mercury

### Windows
1. 打开一个命令行窗口
2. 转到本程序的解压目录
3. 输入以下命令：.\mercury

### Darwin
1. 打开一个命令行窗口
2. 转到本程序的解压目录
3. 输入以下命令：.\mercury

## 基本命令
本程序提供了一个交互式命令行窗口。
![程序界面](./_assets/images/mercury-home.png)

### ls指令
ls指令用于查询当前路径下所有可用的子目录，以及可用的命令。其中
* 子目录：用绿颜色文字标识，包括子目录名称以及描述，并且在Flags栏带d字母。
* 命令：用蓝颜色文字标识，包括命令名称以及描述，并且在Flagsl栏带e字母。

### cd指令
cd指令用于更改当前路径，分三种场景：
1. 进入子目录：在提示符下输入cd dir，其中dir是你要进入的子目录名字。
2. 返回上级目录：在提示符下输入cd .., 表示回到上级目录。
3. 回到根目录：在提示符下输入cd /，表示要回到根目录。

### 执行命令
在提示符下输入可以执行的命令名称即可，比如输入rename即执行rename命令。

### 退出程序
在根目录下，执行exit命令即可退出程序。
