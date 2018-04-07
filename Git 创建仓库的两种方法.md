主要有两种创建 Git 仓库的方法：

1. 远端创建，本地克隆

2. 本地创建，提交到远端

# 1. 在 GitHub 网站上进行仓库创建，克隆到本地

```shell
git clone git@github.com:<username>/<reponame>.git <directory>  # 克隆仓库到指定目录
```

# 2. 在本地进行仓库创建，提交到 GitHub

> 此方法演示了本地仓库的创建过程，如果想提交到远端，仍然需要事先在 GitHub 网站上创建新仓库。

```shell
git init  # 仓库初始化

echo "init repo" >> README.md  # 编写 README.md，GitHub 强制要求不能提交空项目，项目至少应包含 README.md 文件。

git add .  # 将当前目录内的所有文件添加到暂存区，加入跟踪。

git commit -m "init repo"  # 提交到本地库
    -m  commit message

git remote add origin git@github.com:<username>/<reponame>.git  # 添加远程仓库

git push -u origin master  # 提交到远程仓库
```