# windows软件安装
1. 激活工具：最好使用美国ip登录，https://forums.mydigitallife.net/threads/kmspico-official-thread.65739/
  a. 新的激活工具,原来的kmspico不更新了:https://github.com/abbodi1406/KMS_VL_ALL_AIO/releases
2. 安装翻墙工具:
  a. virtual+openwrt:	https://www.virtualbox.org/wiki/Downloads
  b. clash for windows:	https://github.com/Fndroid/clash_for_windows_pkg/tags\
  c. qv2ray:
  d. powershell代理:$env:HTTP_PROXY="http://127.0.0.1:1080"
3. 安装必要软件:
  a. 安装chocolate: https://chocolatey.org/install
  b. notepad++: https://notepad-plus-plus.org/downloads/
  c. vscode: https://code.visualstudio.com/
  d. ffmpeg:https://ffmpeg.org/
  e. mpv:https://mpv.io/
  f. potpalyer:http://potplayer.daum.net/?lang=zh_CN
  g. powertoys:https://github.com/microsoft/PowerToys/releases
  h. wox:https://github.com/Wox-launcher/Wox
  i. telegram:https://github.com/telegramdesktop/tdesktop
  j. you-get,youtube-dl:pip install you-get youtube-dl
  k. clash for windows:https://github.com/Fndroid/clash_for_windows_pkg/releases
  l. google-chrome:https://www.google.com/intl/zh-CN/chrome/
  m. 
  n. wsl2: 
#!/bin/bash
host_ip=$(cat /etc/resolv.conf |grep "nameserver" |cut -f 2 -d " ")
export ALL_PROXY="http://$host_ip:7890"

# 可以直接写在配置文件里
```
export host_ip=$(cat /etc/resolv.conf |grep "nameserver" |cut -f 2 -d " ")
export ALL_PROXY="http://$host_ip:7890"
f. minGW:https://sourceforge.net/projects/mingw-w64/
```