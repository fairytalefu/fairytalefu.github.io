---
title: 将Hexo部署到Coding
tags: hexo
categories: hexo
---
###  1.创建github的仓库
> 登录到GitHub,如果没有GitHub帐号，使用你的邮箱注册GitHub帐号：Build software better, together 点击GitHub中的New repository创建新仓库，仓库名应该为：用户名.http://github.io 这个用户名使用你的GitHub帐号名称代替，这是固定写法，比如我的仓库名为：

``` bash
$ git config --global user.name "fairytalefu"
$ git config --global user.email "fairytalefu@outlook.com"

```

### 2.设置SSH Key
> 查找云服务器的SSH公钥，Linux的话在用户目录吓得.ssh，找到id_rsa.pub，复制里面所有内容，粘贴到Coding。Coding上添加SSH key位置：打开Coding 个人设置页面，新建new SSH Key

```bash
# 网址：https://firecode-01.coding.net/user/account/setting/keys
$ ssh-keygen -t rsa -C "fairytalefu@outlook.com"
#验证
$ ssh -T git@coding.net
#别忘了安装hexo-deployer-git 
$ yarn add hexo-deployer-git 
```

### 3.配置Hexo的deploy

```yaml
deploy:
  type: git
  repo: git@github.com:fairytalefu/fairytalefu.github.io.git
  branch: master
  message: "script auto commit"
```


### 4.创建Github Page
> 注意：github私有仓库创建Github Page是需要付费的。如果之前创建的是私有的，可以在Github的Danage Zone转换


### 5.部署到Github
```bash
$ hexo g && hexo d && hexo s
```

### 6.静态博客的痛点

> 1.图床问题
> 2.文章线上编辑


### 7.Hexo 常用命令
```bash
hexo n == hexo new
hexo g == hexo generate
hexo s == hexo server
hexo d == hexo deploy
```