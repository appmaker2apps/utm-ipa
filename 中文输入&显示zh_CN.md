# 中文输入 & 显示

## 中文显示

### 本地化 locale

生成语言包并指定字符集编码

```shell
# locale 的环境变量的优先级：
# LC_All > LC_TIME、LC_CTYPE …… > LANG
locale
```

### 字体 font

```shell
# 中文字体
pacman -S wqy-zenhei
pacman -S wqy-microhei
# 等宽字体
pacman -S ttf-dejavu
pacman -S adobe-source-code-pro-fonts
# 以下非必需
pacman -S adobe-source-han-sans

```

### 支持中文字符集编码、UTF-8 的终端：KMSCON 终端模拟软件

https://wiki.archlinux.org/index.php/KMSCON_(简体中文)

## 中文输入 inputmethod

```text
命令行模式输入不了中文是3运行级别,Xwindows图形界面是5运行级别。
在3运行级别,也就是系统标准运行级别,只能显示中文,不支持输入中文；
在5运行级别,因为安装了图形界面这个环境,在这个环境下支持中文输入。
```

### 运行级别 runlevel

```text
运行级别0：系统停机状态，系统默认运行级别不能设为0，否则不能正常启动 
运行级别1：单用户工作状态，root权限，用于系统维护，禁止远程登陆 
运行级别2：多用户状态(没有NFS) 
运行级别3：完全的多用户状态(有NFS)，登陆后进入控制台命令行模式 
运行级别4：系统未使用，保留 
运行级别5：X11控制台，登陆后进入图形GUI模式 
运行级别6：系统正常关闭并重启，默认运行级别不能设为6，否则不能正常启动
```
