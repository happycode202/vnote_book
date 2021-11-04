# Gentoo
1. 代理设置：

```
/etc/portage/make.conf

http_proxy="http://127.0.0.1:8889"
https_proxy="https://127.0.0.1:8889"
ftp_proxy="http://127.0.0.1:8889"

emerge执行的时候，用portage这个账户，所以在root用户或者其他用户设置代理是没用的
```

2. 输入法：

```
fcitx5-rime
参考：https://wiki.archlinux.org/index.php/Fcitx5#Installation
```
3. 词典

```
goldendict
```

4. layman

```
gentoo-china-overlay和gentoo-taiwan-overlay目前合并成了gentoo-zh，并且这三个overlay都已经进入了gentoo官方layman数据库。
所以：
- sudo emerge -avt layman

- sudo layman -L 可以查询overlay列表

- sudo layman -a gentoo-zh

- 编辑/etc/portage/make.conf，添加：source /var/lib/layman/make.conf（需要至少添加了一个overlay之后才会有这个make.conf）

事实上，emerge layman之后，就会有一些打印告诉我们上述的步骤。
```