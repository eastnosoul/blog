---
title: Git 的一些常用操作
date: 2024-06-06 12:50:31
categories:
  - 工具
tags:
  - Git
---

# Git 的常用操作

> 具体教程可见 [Git](https://git-scm.com/book/zh/v2).

## 使用前的准备

### 查看 Git 的所有配置以及它们的所在位置

```bash
git config --list --show-origin
```

### 用户信息

```bash
git config --global user.name "username"
git config --global user.email example@example.com
```

### 配置密钥

```bash
ssh-keygen -t rsa -C "xxx@xxx.com" # 然后一直回车
cat ~/.ssh/id_rsa.pub # 复制显示的文字 将其配置到对应的服务器
```

## 获取 Git 仓库

### 本地

在已存在的目录下初始化仓库

```bash
git init
```

### 远程

```bash
git clone <url> # 将 <url> 替换为你所需要克隆的仓库链接
```

## 上传

```bash
git remote add origin <url> # <url> 可以是 https 开头，也可能是 git@ 开头(推荐使用)
git add -A # 将所有文件添加到暂存区
git commit -m 'new message' # 将所有文件提交，提交的描述为“new message”
git push origin branch_name # 将本地仓库推送到远程仓库
```
