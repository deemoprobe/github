# github

github常用操作汇总，主要内容如下：

- 初始化仓库
- 配置仓库
- 提交代码到远程仓库
- 分支操作
- 版本管理和回溯
- 高级操作

由于国内(China)GitHub访问太慢,有事甚至在提交时出现`Timeout`的问题,此时可以用VPN解决问题,当  
国内访问速度上去时再取消代理即可

```shell
# 配置后代理要一直开着
git config --global http.proxy "127.0.0.1:1080"
git config --global https.proxy "127.0.0.1:1080"
# 不需要代理时,注释掉或删除即可
vi ~/.gitconfig
```
