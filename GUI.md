# GUI 图形交互界面

DE 和 WM：
Desktop Enviroment
Window Manager

## X.org(X)

```shell
pacman -S xorg-server xorg-xinit

# 启动 X
```shell
xinit # startx
# 启动时会读取 ~/.xinitrc

```

## WM 窗口管理器

```shell
pacman -S i3-gaps i3-status rxvt-unicode dmenu
```

自动启动设置

```shell
vim ~/.xinitrc
# 添加如下字段
# exic i3

```


### Network manager（nm-applet）

### Font

安装字体

```shell
pacman -S ttf-linux-libertine ttf-inconsolata
pacman -S noto-fonts

```

设置字体配置


```text
font family：
1 serif
2 sans-serif
3 sans
4 monospace

```


```shell
vim ~/.config/fontconfig/fonts.conf

```

## DM

Display manager

```shell
# lightdm
pacman -S lightdm lightdm-gtk-greeter
# 设置跟随系统启动
systemctl enable lightdm.service
```

## DE

### xfce4


```shell
pacman -S xfce4
vim ~/.xinitrc
# exec xfce4-session
```


