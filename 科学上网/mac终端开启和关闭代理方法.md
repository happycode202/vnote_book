# mac终端开启和关闭代理方法

#### 别名

```
alias openproxy="export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890 && echo 'set proxy successfully'"
alias closeproxy="unset http_proxy unset https_proxy unset all_proxy && echo 'unset proxy successfully'"
```
#### 脚本

```
在~/.command/路径下，创建两个文件，openproxy.sh 和closeproxy.sh
openproxy.sh
export https_proxy=http://127.0.0.1:7890
export http_proxy=http://127.0.0.1:7890 
export all_proxy=socks5://127.0.0.1:7890
echo "already open proxy with 127.0.0.1:7890"
closeproxy.sh
unset http_proxy
unset https_proxy
unset all_proxy
echo "already close proxy"
修改别名
alias openproxy="source ~/.command/openproxy.sh"
alias closeproxy="source ~/.command/closeproxy.sh"
```

#### 大量抄袭：https://yuhenabc.com/2018/12/29/proxy/