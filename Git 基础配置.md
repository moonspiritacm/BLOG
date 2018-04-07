# 1. 绑定 GitHub 远程仓库

本地仓库可以与远程仓库绑定，充分发挥分布式版本控制系统的优势，这里选用 GitHub。

Git 没有提供专门的传输协议，通常使用 HTTP 协议进行数据传输。出于安全考虑，使用 SSH 进行传输加密。

绑定远程仓库的一般流程是：本地生成公私钥 -> 将公钥上传到 GitHub 服务器 -> 测试连接。

```shell
ssh-keygen -t rsa -C "xxx@gmail.com"  #生成公私钥对
    -t  dsa | ecdsa | ed25519 | rsa  指定加密算法
    -C  comment  添加注释/注解（一般为所有者邮箱）

ssh -T git@github.com  #连通测试
```

# 2. Git 本地环境配置

`git config` 工具用于查看和修改 Git 配置信息，操作分为三个级别：

- 系统级配置，`--system` 选项，读写 /etc/gitconfig 文件，该配置对所有用户生效。

- 用户级配置，`--global` 选项，读写 ~/.gitconfig 文件，该配置对当前用户生效。

- 项目级配置，`--local` 选项，读写当前仓库目录下的 .git/config 文件，该配置仅对当前项目生效。

```shell
git config --global user.name "xxx"  #配置用户名

git config --global user.email "xxx@gmail.com"  #配置用户邮箱
```

配置文件间存在层级覆盖关系，即各级配置会覆盖上级配置文件中的相同变量。

> Windows 系统中各配置文件所在位置：
1. 系统级配置文件：对应 Linux 系统中的 `/etc/gitconfig`，位于 Git 安装目录下。
例如 `D:\Program\Git\mingw64\etc\gitconfig`。
2. 用户级配置文件：对应 Linux 系统中的 `~/.gitconfig`，位于用户根目录下。
例如 `C:\Users\xxx\.gitconfig`。