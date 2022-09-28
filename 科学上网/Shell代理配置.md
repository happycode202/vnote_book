# shell代理配置

## zsh/bash

```bash
export http_proxy=http://127.0.0.1:7890
export https_proxy=https://127.0.0.1:7890
# 或
export all_proxy=socks5://127.0.0.1:7890

# 或
setProxy(){
  export http_proxy=http://127.0.0.1:7890
  export https_proxy=https://127.0.0.1:7890,
  # 或
	export all_proxy=socks5://127.0.0.1:7890
	echo "All proxy on"
}
unsetProxy(){
	unset all_proxy
	echo "All proxy off"
}
```

## fish

```bash
function setProxy
	set -xg ALL_PROXY http://localhost:7890
	echo "proxy on"
end

function unsetProxy
	set -e ALL_PROXY
	echo "proxy off"
end
```

## PowerShell

```cmd
echo $profile	#查看配置文件路径
Test-Path $profile	#测试文件路径,看配置文件是否存在
New-Item -Path $profile -Type File –Force	#新项 配置文件路径 配置文件类型 文件强制
function proxy() {
  $Env:https_proxy="http://localhost:7890"
  $Env:http_proxy="http://localhost:7890"
}
function noproxy() {
  $Env:https_proxy=""
  $Env:http_proxy=""
}
```

## Git

```bash
# 设置
git config --global https.proxy http://127.0.0.1:7890
git config --global https.proxy https://127.0.0.1:7890
​
# 取消
git config --global --unset http.proxy
git config --global --unset https.proxy
```





