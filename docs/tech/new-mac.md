
新苹果电脑环境配置

# SSH 远程登录

首次 SSH 远程操作之前，需手动执行一次命令：`ssh {USERNAME}@{IP}`，否则每次都需要进行交互式输入密码

```sh
# 远程登录
# USERNAME 是要连接主机的用户名
# IP 是要连接主机的IP地址
ssh {USERNAME}@{IP}
```

[ssh sshpass scp 使用实例](http://gitlab.ft.com/-/ide/project/CISys/CI_Package_Tool/tree/develop/-/CloudPhone.sh/)

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

> 增量同步、可定时 StageMirror

同步软件：[Sync Folders Pro 4.5.9 文件夹同步工具](https://xclient.info/s/sync-folders-pro.html)

自己开发脚本
1. rsync 同步
2. 添加定时任务
3. 提交到 Git

相关文章参考
- https://blog.csdn.net/xu710263124/article/details/120288898
- https://blog.csdn.net/vic_qxz/article/details/103019771
- https://blog.csdn.net/weixin_43889439/article/details/96337953
- https://blog.csdn.net/Little_fxc/article/details/102779983
- https://blog.csdn.net/weixin_45491473/article/details/121706221

# You have new mail.
新建终端窗口，第一句是 *You have new mail.*
解决办法：
1. 查看待发送的 email，终端输入 `mail` 回车
2. 打开文件夹 `/var/mail/`，删除里面的文件
3. 再次新建终端窗口，这句话消失

# 查看终端命令历史记录

```sh
# 查看最近的终端执行命令
history
```

```sh
# 查看所有的终端执行命令
history 0
```

```sh
# 查看所有的终端执行命令，并显示执行时间
HISTTIMEFORMAT='%F %T ' history -i 0
```

如果您使用 bash，查看文件 `~/.bash_history`
如果您使用 zsh，查看文件 `~/.zsh_history`
将历史记录的输出重定向到文件 `history > history.txt`
[MacOS zsh history命令显示操作时间](https://blog.csdn.net/WoBenZiYou/article/details/101465171)
[linux/macOS 中history命令显示执行时间](https://www.jianshu.com/p/324bcacca486)

# Chrome浏览器前进后退手势
在系统偏好设置/鼠标或触控板/在页面之间轻扫，开启该项

# 时间机器
Time Machine （时间机器）是 Mac 的内置备份功能。您可以使用 Time Machine 对您的所有文件进行自动备份，包括应用、音乐、照片、电子邮件、文稿和系统文件。如果您拥有备份，当原始文件从 Mac 永久性删除或者 Mac 中的硬盘（或 SSD）被抹掉或更换时，可以从备份恢复文件。

[Time Machine 使用方法](https://www.jb51.net/softjc/676703.html)

# 网络
- 公司网络屏蔽了部分网站，导致有的网站访问不了、有的软件使用不了
- 有的网站需要翻墙，需要[切换线路](http://it.ft.com/tool/egress)

# 备份
- 备份整个系统： Time Machine
- 备份书签、密码、扩展程序
    - Google Chrome 账号
- 备份应用程序
    - https://github.com/lra/mackup
    - https://sspai.com/post/32933
    - https://blog.csdn.net/mangocream/article/details/42497073
- 备份 Atom 配置
    - [Sync Settings](https://atom.io/packages/sync-settings)

# 网站
将网站添加到书签，使用 Chrome 同步数据

# 软件
- 超级右键
- 微信
- Atom
- [Dr. Unarchiver v1.3.0](https://www.macbl.com/app/utilities/dr.-unarchiver)
- [Go2Shell](https://zipzapmac.com/Go2Shell)
  - 官网 https://zipzapmac.com/Go2Shell
  - 网盘 https://blog.csdn.net/shentian885/article/details/106327349/
  - 升级 https://my.oschina.net/1715828751/blog/4785100
  - /Applications/Go2Shell.app/Contents/MacOS
- Google Chrome
- [Paste](https://www.macfz.com/a/Paste.html)
  Mac上“您没有权限来打开应用程序”（Big Sur）
  https://www.cnblogs.com/somefuture/p/14085569.html
- Sublime Text
- Sync Folders Pro
- Tencent Lemon
- Tower v4.3 *城通网盘*、*腾讯微云，微信账号*
- Unsplash Wallpapers
- WPS Office
- Xnip
- QQ影音
- iRelax
- [唐师父](https://www.zjyunkai.com/macload?es=138&ct=1)
- Xcode
`xcode-select --install`

pod setup 操作失败
Setup completed
解决办法：`git clone https://github.com/CocoaPods/Specs.git ~/.cocoapods/repos/trunk`

**需破解的软件，必须存储到百度网盘、城通网盘等平台**

已损坏,⽆法打开。 您应该将它移到废纸篓。
```sh
sudo spctl --master-disable
sudo xattr -d com.apple.quarantine /Applications/xxxx.app
```

# Chrome 扩展程序

# 命令行
- [homebrew](https://brew.sh/)
    brew 换源
    https://www.jianshu.com/p/8a2ac505ff3e
    https://lug.ustc.edu.cn/wiki/mirrors/help/brew.git/
    安装Homebrew失败
    https://www.cnblogs.com/china-baizhuangli/p/12729494.html
- tree
    `brew install tree`
    `tree -L 1` 查看文件夹下的第一层文件
- node
    `brew install node`
    如果遇到 node 依赖库安装失败，先单个安装该依赖库
- [npm](https://www.yuque.com/u191966/program/ps4coe)
    node 已内置 npm
    `npm search`报错解决办法：`npm search {NAME} --registry=https://registry.npmjs.org`
- yarn
    `npm install -g yarn`
- docsify
    `npm i docsify-cli -g`
- gem
- [cocoapods](https://www.yuque.com/u191966/apple/sqnwf8)
  https://gems.ruby-china.com/
  https://v.qq.com/x/page/d0352io5rcb.html

[mac 修改主机名和计算机名 terminal终端、iterm前⾯的⽤户名字](https://liuchuo.blog.csdn.net/article/details/79967956)
百度搜索：隐藏名字 Mac和终端中的⽤户名- macOS

# Atom

Packages:
- color-picker
- file-icons
- highlight-selected
- [markdown-preview-enhanced](https://shd101wyy.github.io/markdown-preview-enhanced/#/zh-cn/)
- platformio-ide-terminal
- split-diff
- sync-settings
- tool-bar
- tool-bar-atom
- activate-power-mode

Theme:
- Genesis
- Atom Material

styles.less
```css
.tree-view {
  // background-color: whitesmoke;
  font-size: 15px;
  font-family: Andale mono; // Andale mono, Menlo, Consolas, DejaVu Sans Mono, monospace
}

.tab-bar .tab, .tab.active .title {
    font-size: 14px;
    font-family: Andale mono;
}

.settings-view, .status-bar {
    font-size: 12px;
    font-family: Andale mono;
}
```

# 系统
- [x] [GitHub](https://github.com/settings/tokens)
- [x] GitLab

# 快捷键
[快速打开系统偏好设置](http://news.sohu.com/a/501927306_120371013)
1. 打开'系统偏好设置 > 键盘 > 快捷键'，找到 'App快捷键'，点击下方的 '+'
2. 应用程序选择 `所有应用程序`，菜单标题为 `系统偏好设置...` (英文输入法下按Optiont+;)
3. 最后设置一个自己喜欢的快捷键，比如 `⇧⌘,` 点击添加
4. 设置完成后，注销或者重启即可使用

切换到桌面的快捷键：
打开'系统偏好设置 > 键盘 > 快捷键 > 调度中心'，设置'显示桌面'的快捷键为 `⌘D`
