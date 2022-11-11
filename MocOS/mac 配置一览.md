# mac 配置一览

## conda 代理配置

```zsh
$ touch .condarc
channels:
  - defaults
show_channel_urls: true
default_channels:
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
custom_channels:
  conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  pytorch-lts: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
```

## 防止触控板误触

> 1. 安装电池,让系统将机器识别为笔记本
> 2. 辅助功能->指针控制->勾选 当连接鼠标时禁用触控板

## 开启触控板点触

> System Preference -> touchpad -> 勾选点触

## 开启触控板拖动

> 辅助功能->指针控制-> 触控板设置 勾选鼠标拖动并设置拖移锁定

## 管理 python 虚拟环境

```bash
$ python -m venv [name]
# 在当前文件夹内创建名为[name]的虚拟环境管理文件
$ source [name]/bin/activate
# 载入配置
# 删除虚拟环境 直接删除文件夹就行
$ trash -F [name]
```

## zsh 粘贴长文/长命令速度慢

> 由于之前在zsh装了几个插件，只要terminal里粘贴内容，就非常的卡，基本上是一秒上屏一个字符，查了一下，正是由**zsh-autosuggestions**插件引起的，在官方的**238**号issue里有解决方法
>
> ```zsh
> 
> # This speeds up pasting w/ autosuggest
> # https://github.com/zsh-users/zsh-autosuggestions/issues/238
> pasteinit() {
>   OLD_SELF_INSERT=${${(s.:.)widgets[self-insert]}[2,3]}
>   zle -N self-insert url-quote-magic # I wonder if you'd need `.url-quote-magic`?
> }
> 
> pastefinish() {
>   zle -N self-insert $OLD_SELF_INSERT
> }
> zstyle :bracketed-paste-magic paste-init pasteinit
> zstyle :bracketed-paste-magic paste-finish pastefinish
> ```
>
