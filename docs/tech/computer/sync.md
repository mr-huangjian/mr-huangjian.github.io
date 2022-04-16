# 同步
---

# SSH 远程登录

首次 SSH 远程操作之前，需手动执行一次命令：`ssh {USERNAME}@{IP}`，否则每次都需要进行交互式输入密码

```sh
# 远程登录
# USERNAME 是要连接主机的用户名
# IP 是要连接主机的IP地址
ssh {USERNAME}@{IP}
```

# SCP 远程拷贝

```sh
# 拷贝本地文件到远程主机
# FILE_SOURCE_PATH 本地主机要拷贝的原文件的绝对路径
# FILE_TARGET_PATH 远程主机存储拷贝文件的绝对路径
# USERNAME 是要连接主机的用户名
# IP 是要连接主机的IP地址
# 可以本地主机连接本地主机进行测试
scp {FILE_SOURCE_PATH} {USERNAME}@{IP}:{FILE_TARGET_PATH}
```

```sh
# 拷贝本地文件夹到远程主机
# FOLDER_SOURCE_PATH 本地主机要拷贝的原文件夹的绝对路径
# FOLDER_TARGET_PATH 远程主机存储拷贝文件夹的绝对路径
scp -r {FOLDER_SOURCE_PATH} {USERNAME}@{IP}:{FOLDER_TARGET_PATH}
```

# 本机两个文件夹同步

同步软件：[Sync Folders Pro 4.5.9 文件夹同步工具](https://xclient.info/s/sync-folders-pro.html)

自己开发脚本
1. rsync 同步
2. 添加定时任务
3. 提交到 Git

<details>
<summary>rsync 定时增量备份到 Git</summary>
<li> https://blog.csdn.net/xu710263124/article/details/120288898</li>
<li> https://blog.csdn.net/vic_qxz/article/details/103019771</li>
<li> https://blog.csdn.net/weixin_43889439/article/details/96337953</li>
<li> https://blog.csdn.net/Little_fxc/article/details/102779983</li>
<li> https://blog.csdn.net/weixin_45491473/article/details/121706221</li>
</details>
<br>

# 其他
[ssh/sshpass/scp 使用实例](http://gitlab.ft.com/-/ide/project/CISys/CI_Package_Tool/tree/develop/-/CloudPhone.sh/)
