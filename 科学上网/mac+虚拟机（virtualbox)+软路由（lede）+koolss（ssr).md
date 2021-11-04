# mac+虚拟机（virtualbox)+软路由（lede）+koolss（ssr)


1. lede镜像下载地址:https://firmware.koolshare.cn/LEDE_X64_fw867/虚拟机转盘或PE下写盘专用/openwrt-koolshare-mod-v2.31-r10822-50aa0525d1-x86-64-combined-squashfs.img.gz
2. 解压镜像:双击即可,将镜像文件的后缀名改为.hdd
3. 创建虚拟机:
  ○ 新建虚拟机---->类型:linux 版本:other-linux---->内存:1024Mb---->使用已有的虚拟硬盘文件----> 添加镜像----> 选择添加镜像----> 创建
  ○ 系统:    删除软盘/光驱/
  ○ 处理器:    1
  ○ 声音:    删除声卡
  ○ 网络:    桥接网卡 wifi
  ○ 启动
4. 配置lede
  ○ 配置ip
  
```
vim /etc/config/network

    option ipaddr '192.168.1.xxx
    config interface 'lan'
```

  ○ web端登陆配置
    ■ 地址:192.168.1.xxx    用户名:root    密码:koolshare
    ■ 网络---->接口---->lan---->编辑
      ● ipv4网关:192.168.1.1
      ● 使用自定义dns
        ```
        ○ 114.114.114.114
        ○ 233.5.5.5
        ○ 8.8.8.8
        ```
      ● 保存并应用
    ■ 酷软
      ● 更新系统
5. ss安装
  a. 软件下载:https://github.com/hq450/fancyss_history_package/tree/master/fancyss_X64
  b. 离线安装:
    ■ 选择安装包---->选择软件---->选择下载的koolss---->上传并安装---->添加节点
6. 本地网络配置
  a. 网络配置
    ⅰ. TCP/IP
      1. 配置IPv4:手动
      2. ipv4地址:192.168.1.xxx-1
      3. 子网掩码:255.255.255.0
      4. 路由器:192.168.1.xxx (此处地址和上面的ipaddr/web端登录地址    一致)
      5. dns服务器地址:和上面的一致