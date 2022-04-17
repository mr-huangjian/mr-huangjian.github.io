# Git

## 登录认证

- [GitHub Personal access tokens](https://github.com/settings/tokens)
- [GitLab Personal access tokens]()

Personal Access Tokens 是通用的，<u>**可以保存下来，避免每次重新生成**</u>！

## 安全传输
- [GitHub SSH key](https://github.com/settings/keys)
- [GitLab SSH key]()

SSH 是一种安全的传输模式。

Github 要求推送代码的用户是合法的，所以每次推送时候都要输入账号密码，用以验证你是否为合法用户，为了省去每次都要输入密码的步骤，采用 SSH 公钥、密钥，也就是你说的 SSH key 来验证你是否为合法用户。

在你的电脑生成了一个唯一的 SSH 公钥和私钥，公钥放到 Github 上面，当你推送的时候，Git 就会匹配你的私钥，是跟 Github 上面的公钥是配对的，正确就认为你是合法的，允许推送。

SSH key 可以理解为是你的身份标识，放在 Github 上面表明你是这个项目的一个开发人员，但是别人是可以截获的，你本机的私钥别人就无法截获，SSH key 就可以保证每次传输都是安全的。
