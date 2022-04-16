
# You have new mail.
新建终端窗口，第一句是 *You have new mail.*
解决办法：
1. 终端输入 `mail` 回车，查看待发送的 email
2. 打开文件夹 `/var/mail/`，删除里面的文件
3. 再次新建终端窗口，这句话消失

# 命令

## homebrew
[官网](https://brew.sh/) / [换源](https://www.jianshu.com/p/8a2ac505ff3e) / [中科大源](https://lug.ustc.edu.cn/wiki/mirrors/help/brew.git/) / [安装失败](https://www.cnblogs.com/china-baizhuangli/p/12729494.html)

## tree
`brew install tree`<br>
`tree -L 1` 查看文件夹下的第一层文件

## node
`brew install node`<br>
如果遇到 node 依赖库安装失败，先单个安装该依赖库

## npm
[官网](https://www.npmjs.cn/) node 已内置 [npm](https://www.yuque.com/u191966/program/ps4coe)<br>
`npm search`报错解决办法：`npm search {NAME} --registry=https://registry.npmjs.org`

## yarn
[官网](https://www.yarnpkg.cn/) `npm install -g yarn`

## docsify
[官网](https://docsify.js.org/#/zh-cn/quickstart) `npm i docsify-cli -g`

## cocoapods
[介绍](https://www.yuque.com/u191966/apple/sqnwf8) / [视频教程](https://v.qq.com/x/page/d0352io5rcb.html)

# 自定义命令
在 `~/.bash_profile` 文件下添加该行，若该文件不存在则需自己创建。<br />等号左边是命令名称，右边是具体命令或具体实现的文件路径。

- 示例 1

```
alias npmpub="npm publish"
```

```shell
$ npmpub
```

- 示例 2

```
alias npmpub="~/Documents/shell/npm-publish.sh"
```

```shell
$ npmpub arg1 arg2 arg3
```

如果保存好后命令不生效，则执行命令 `source ~/.bash_profile` 后再尝试执行。

# 记录

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

如果您使用 bash，查看文件 `~/.bash_history`<br>
如果您使用 zsh，查看文件 `~/.zsh_history`<br>
将历史记录的输出重定向到文件 `history > history.txt`<br>

[MacOS zsh history命令显示操作时间](https://blog.csdn.net/WoBenZiYou/article/details/101465171) / [linux/macOS 中history命令显示执行时间](https://www.jianshu.com/p/324bcacca486)

# 其他
- [mac终端～%切换～$](https://blog.csdn.net/qq_31954797/article/details/111601223)
- [mac 修改主机名和计算机名 terminal终端、iterm前⾯的⽤户名字](https://liuchuo.blog.csdn.net/article/details/79967956)
