# Windows常见问题集锦

## 激活工具：

- [kmspico](https://forums.mydigitallife.net/threads/kmspico-official-thread.65739/)
- [KMS_VL_ALL_AIO](https://github.com/abbodi1406/KMS_VL_ALL_AIO/releases)

## 翻墙(&代理)工具:

- [virtual+openwrt](https://www.virtualbox.org/wiki/Downloads)  
- [Qv2ray](https://github.com/Qv2ray/Qv2ray)+[v2ray](https://github.com/v2ray/v2ray-core)
- [clash for windows pkg](https://github.com/Fndroid/clash_for_windows_pkg)
- [V2rayN](https://github.com/2dust/v2rayN)

## 必要软件:

- [安装chocolate](https://chocolatey.org/install)
- [notepad++](https://notepad-plus-plus.org/downloads/)
- [uTools](https://u.tools/)
- [notepad++](https://notepad-plus-plus.org/downloads/)  
- [vscode](https://code.visualstudio.com/)  
- [ffmpeg](https://ffmpeg.org/)  
- [mpv](https://mpv.io/)  
- [potpalyer](http://potplayer.daum.net/?lang=zh_CN)  
- [powertoys](https://github.com/microsoft/PowerToys/releases)  
- [wox](https://github.com/Wox-launcher/Wox)  
- [telegram](https://github.com/telegramdesktop/tdesktop)  
- you-get,youtube-dl:pip install you-get youtube-dl  
- [clash for windows](https://github.com/Fndroid/clash_for_windows_pkg/releases)  
- [google-chrome](https://www.google.com/intl/zh-CN/chrome/)   
- [minGW](https://sourceforge.net/projects/mingw-w64/)
- [JDK](https://repo.huaweicloud.com/openjdk/)
- [microsoft](https://github.com/microsoft)/**[terminal](https://github.com/microsoft/terminal)**
- [PowerShell](https://github.com/PowerShell)/**[PowerShell](https://github.com/PowerShell/PowerShell)**
- [microsoft](https://github.com/microsoft)/**[PowerToys](https://github.com/microsoft/PowerToys)**
- wsl2

```bash
#!/bin/bash
host_ip=$(cat /etc/resolv.conf |grep "nameserver" |cut -f 2 -d " ")
export ALL_PROXY="http://$host_ip:7890"
#可以直接写在配置文件里
export host_ip=$(cat /etc/resolv.conf |grep "nameserver" |cut -f 2 -d " ")
export ALL_PROXY="http://$host_ip:7890"
```

## PowerShell配置

1. 当前主机，当前用户的配置

   ```powershell
   if (!(Test-Path -Path $PROFILE)) {
     New-Item -ItemType File -Path $PROFILE -Force
   }
   ```

  2. 配置代理

     ```powershell
     $ notepad++ $profile 
     添加代理
     $env:HTTP_PROXY="http://127.0.0.1:7890"
     $env:HTTPS_PROXY="http://127.0.0.1:7890"
     $env:ALL_PROXY="http://127.0.0.1:7890"
     ```

     
