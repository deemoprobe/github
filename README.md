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

目前(2.28版本)git默认分支已经由`master`切换到`main`,可以使用下面命令将使用git时默认指向分支切换为main

```shell
git config --global init.defaultBranch main
# 查看配置
vi ~/.gitconfig
```

5步把GitHub上的git仓库的默认分支从`master`切换到`main`

1. 本地把分支从`master`切换到`main`

    ```shell
    git branch -m master main
    ```

2. 把`main`分支推送到远程仓库

    ```shell
    git push -u origin main
    ```

3. 将仓库的`HEAD`指向`main`分支

    ```shell
    git symbolic-ref refs/remotes/origin/HEAD refs/remotes/origin/main
    ```

4. 修改GitHub的默认分支

    ```shell
    在GitHub上对应仓库"Settings" -> "Branches",修改默认分支名
    ```

5. 删除`master`分支

    ```shell
    git push origin --delete master
    or
    git push origin :master
    ```
