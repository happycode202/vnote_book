# powershell配置

## 当前主机，当前用户的配置文件
```powershell
if (!(Test-Path -Path $PROFILE)) {
  New-Item -ItemType File -Path $PROFILE -Force
}
```
## 代理配置

打开上面新建的配置文件
```powershell
$ notepad $profile 
添加代理
$env:HTTP_PROXY="http://127.0.0.1:7890"
$env:HTTPS_PROXY="http://127.0.0.1:7890"
$env:ALL_PROXY="http://127.0.0.1:7890"
```