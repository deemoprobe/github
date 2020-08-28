# GitHub常用操作命令

## Git和GitHub

git是分散型版本管理系统，GitHub为开发者提供Git仓库的托管服务，社会化协作编程平台。

## 准备

- 安装Git
- 安装vscode（Linux平台忽略此操作）
- 注册GitHub
- Git初始设置
- 配置SSH Key

### Git初始设置

```shell
# git全局配置
git config --global user.name your.name
git config --global user.email your.email
git config --global color.ui auto
# 查看配置
cat ~/.gitconfig
```

### 配置SSH Key

```shell
# 创建SSH Key
ssh-keygen -t rsa -C "your.email"
# Generating public/private rsa key pair...
# 三次回车即可生成 ssh key

# 在GitHub添加公钥（public key）
cat ~/.ssh/id_rsa.pub
# 复制公钥内容
在[设置页面](https://github.com/settings/keys)新建SSH Key认证，名称自定义，把公钥内容粘贴进去
# 公钥私钥认证通信（建立与GitHub连接）
ssh -T git@github.com
# 出现Hi your.name...等输出则配置成功
```

## Git操作

```shell
# 准备好项目工程空目录/projects/github/
cd ./projects/github/
# 仓库初始化
git init
# 创建自己的工程文件
...
# 暂存区添加自己的文件
git add file.name
# 
```
