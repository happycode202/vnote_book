# git常见问题

## 下载安装
[下载地址](https://git-scm.com/downloads)

## 本地配置
```
git config --global user.name "learn2021-coder"
git config --global user.email "sunhongleisun1@protonmail.com"
```

## 生成密钥
```
ssh-keygen -t rsa -C "sunhongleisun1@protonmail.com"
```
## 添加公钥到github（setting——ssh and gpg keys)
## 拉取并链接远程仓库
```
git clone git@github.com:learn2021-coder/vnote_book.git (拉取远程库)

```
按照这个顺序操作下来，从远程拉取下来的远程库已经能够正常操作，可以用git push测试下。
