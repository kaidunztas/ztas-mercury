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
3. 输入以下命令：./mercury

### Windows
1. 打开一个命令行窗口
2. 转到本程序的解压目录
3. 输入以下命令：.\mercury.exe

### Darwin
1. 打开一个命令行窗口
2. 转到本程序的解压目录
3. 输入以下命令：./mercury

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

## 功能说明

### 注册域
组织机构要用本平台的零信任访问服务之前，第一步要先注册组织机构的域。
要注册域，需要在本命令行窗口的根目录输入执行以下步骤：

```
1. 输入reg命令
2. 出现提示，要求你输入Domain ID，请输入一个以"."分割的域名，比如abc.com, abc.org等，类似于互联网的顶级域名。
3. 在输入组织机构名称，比如"abc company"。
4. 如果域名注册成功，会提示相应的信息，否则会提示域名已存在。
```

### 用户管理
域创建成功后，要对域下的用户进行管理。每个域有一个管理员账号。

从根目录执行cd users命令，即可进入用户管理界面。


![用户管理](_assets/images/mercury-users-home.png)

注意：

<font color="red">每个用户有一个唯一的令牌，令牌由16个字符构成，用户凭借该令牌登录平台，因此，每个用户的令牌需要妥善保管，一旦令牌丢失，将无法访问该平台。</font>

可执行命令列表

![命令列表](_assets/images/mercury-users-commands.png)

* add: 添加域用户
* open: 从当前页打开指定的域用户
* next: 显示下一页域用户列表
* prev: 显示上一页域用户列表
* cur: 显示当前页域用户列表

#### 添加用户
在用户管理界面输入add命令，程序会出现如下的界面：

![添加用户](_assets/images/mercury-users-add.png)

用户创建成功后，系统会提示该用户的令牌。

#### 打开用户
在用户管理界面输入open命令，程序会显示如下界面，让你选择要打开的用户：

![选择用户](_assets/images/mercury-users-select.png)

选择以后，摁回车，即打开该用户，进入该用户的管理界面。

![打开用户](_assets/images/mercury-users-open.png)

用户管理界面提供以下几个命令：
* token: 显示当前[用户的令牌](#token)
* reset: [重设](#reset)当前用户的令牌
* info: 显示当前用户的信息
* del: 删除当前用户

#### <a name="token">显示用户令牌</a>
用户令牌是用户访问平台的唯一凭证，令牌由16个字符组成，由平台随机生成，平台内唯一。因此用户的令牌需要由用户妥善保管。

在打开用户后，在命令行窗口输入token命令，系统会显示当前用户的令牌。

#### <a name="reset>重设用户令牌</a>
在打开用户后，在命令行窗口输入reset命令，系统会显示如下的界面，让你确认是否要重设令牌，当选择Yes后，即可重设当前用户的令牌，并且使原有的令牌失效。

![重设令牌](_assets/images/mercury-users-reset.png)


注意：<font color="red">当用户的令牌重设后，通过该令牌登录的程序，都要重新输入新令牌。</font>
