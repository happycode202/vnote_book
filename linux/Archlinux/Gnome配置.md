# Gnome配置
1. pop-shell
```
gnome-shell-extension-pop-shell-git
https://github.com/pop-os/shell#overridden-gnome-shortcuts
```

2. 快捷键设置(最简单的方法是使用dconf-editor)
```
gsettings set org.gnome.desktop.wm.keybindings toggle-maximized "['<Super>m']"
最大化窗口切换
gsettings set org.gnome.desktop.wm.keybindings close "['<Super>q']"
关闭当前程序
gsettings set org.gnome.desktop.wm.keybindings show-desktop "['<Super>d']"
显示桌面
```

3. 软件
`yay -S v2raya xray fzf mpv youtube-dl you-get zsh oh-my-zsh-git zsh-autosuggestions zsh-syntax-highlighting fontweak otf-fira-sans google-chrome otf-fira-mono nvidia-prime` 
4. popshell 的launcher为pop-launcher 快捷键可直接通过搜索锁定