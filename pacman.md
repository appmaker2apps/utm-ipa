# pacman

## 备份和还原

```shell
# 备份
pacman -Qqen > packages-repository.txt
pacman -Qqem > packages-AUR.txt
# 还原
pacman --needed -S - < packages-repository.txt 
cat packages-AUR.txt | xargs yaourt -S --needed --noconfirm
```

## 安装 Git

```shell
pacman -S git
```

## 安装 Tmux

```shell
pacman -S tmux
# tmux: invalid LC_ALL,LC_CTYPE, or LANG …… 问题解决
# 检查已经开启的设置
locale -a

vim /etc/locale.gen
# 取消注释 en_US.UTF-8 UTF-8
locale-gen
# 系统 locale
# /etc/locale.conf
```

## 安装 Python

```shell
# 默认安装 Python 3
pacman -S python
# 单独安装 pip
pacman -S python-pip
```

## 安装 openssh

```shell
pacman -Sy openssh
systemctl restart sshd
systemctl enable sshd
```

## 安装 Oh My Zsh

```shell
sudo pacman -Sy zsh git
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```