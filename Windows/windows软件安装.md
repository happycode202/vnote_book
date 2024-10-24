# Windows软件安装

## 激活工具：

- [kmspico](https://forums.mydigitallife.net/threads/kmspico-official-thread.65739/)
- [KMS_VL_ALL_AIO](https://github.com/abbodi1406/KMS_VL_ALL_AIO/releases)

## 免费机场

- [yu-steven/*openit*](https://github.com/yu-steven/openit)

  ```
  Base64 https://openit.daycat.space/long
  
  小火箭 https://openit.daycat.space/https
  
  Clash https://openit.daycat.space/clash
  
  Quanx https://openit.daycat.space/qx
  
  ```

  

## 翻墙(&代理)工具:

- [virtual](https://www.virtualbox.org/wiki/Downloads)  
- [openwrt](https://drive.google.com/drive/folders/1dqNUrMf9n7i3y1aSh68U5Yf44WQ3KCuh)
- [Qv2ray](https://github.com/Qv2ray/Qv2ray)+[v2ray](https://github.com/v2ray/v2ray-core)
- [clash for windows pkg](https://github.com/Fndroid/clash_for_windows_pkg)
- [V2rayN](https://github.com/2dust/v2rayN)

## 必要软件:
- [安装localsend](https://localsend.org/zh-CN/download)
- [安装scoop](https://scoop.sh/)
- [winget](https://github.com/microsoft/winget-cli)
- [uTools](https://u.tools/)   
- [microsoft](https://github.com/microsoft)/**[terminal](https://github.com/microsoft/terminal)**
- [PowerShell](https://github.com/PowerShell)/**[PowerShell](https://github.com/PowerShell/PowerShell)**
- [microsoft](https://github.com/microsoft)/**[PowerToys](https://github.com/microsoft/PowerToys)**

## winget 安装必要软件

- 生成安装命令的网站:`https://winstall.app/generate`

```powershell
 winget install --id=voidtools.Everything -e  ; winget install --id=Thunder.Thunder -e  ; winget install --id=EuSoft.Eudic -e  ; winget install --id=Microsoft.VisualStudioCode -e  ; winget install --id=Telegram.TelegramDesktop -e   ; winget install --id=Daum.PotPlayer -e  ; winget install --id= 9P2W3W81SPPB -e ;winget install --id=GitHub.GitHubDesktop -e  ; winget install --id=Tencent.Foxmail -e  ; winget install --id=Tencent.QQ.NT -e  ; winget install --id=Vivaldi.Vivaldi -e  ; winget install --id=Tencent.WeChat -e  ; winget install --id=Bitwarden.Bitwarden -e  ; winget install --id=Baidu.BaiduNetdisk -e  ; winget install --id=Alibaba.aDrive -e  ; winget install --id=Emurasoft.EmEditor -e  ; winget install --id=Sogou.SogouInput -e  ; winget install --id=Rime.Weasel -e ;winget install --id=Git.GIt -e;winget install --id=Microsoft.PowerShell -e  ;
```

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
   echo $profile	#查看配置文件路径
   Test-Path $profile	#测试文件路径,看配置文件是否存在
   New-Item -Path $profile -Type File –Force	#新项 配置文件# 路径 配置文件类型 文件强制
   
   
chcp 65001
function openproxy() {
   $Env:https_proxy="http://localhost:7897"
   $Env:http_proxy="http://localhost:7897"
}
function closeproxy() {
    $Env:https_proxy=""
    $Env:http_proxy=""
}
New-Alias -Name note -Value emeditor
#New-Alias -Name huya -Value $HOME\Documents\zhibo\huya.bat
#oh-my-posh init pwsh --config C:\Users\sunho\amro.omp.json | Invoke-Expression
New-Alias -Name m3u8 -Value D:\tools\N_m3u8DL-RE_Beta_win-x64\N_m3u8DL-RE
Set-PSReadLineOption -EditMode Emacs  #启用linux风格的快捷键
   
   ```
