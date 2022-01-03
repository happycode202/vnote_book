# ArchLinux+plasma

## 常用软件安装配置

### 安装
$ fcitx5-im fcitx5-material-color fcitx5-chinese-addons visual-studio-code-bin libva-intel-driver google-chrome nvidia nvidia-prime telegram-desktop xdman noto-fonts noto-fonts-cjk noto-fonts-emoji ttf-sarasa-gothic


### 配置

```bash
$ $HOME/.xprofile

export GTK_IM_MODULE=fcitx5
export QT_IM_MODULE=fcitx5
export XMODIFIERS=@im=fcitx5
```

```bash
$ $HOME/.config/chrome-flags.conf
--ignore-gpu-blocklist
--enable-gpu-rasterization
--enable-zero-copy
--enable-features=VaapiVideoDecoder
--use-gl=egl

```

```bash
$ $HOME/.config/fontconfig/fonts.conf
```

