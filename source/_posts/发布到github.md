---
title: hexo发布到github
tags: hexo
categories: hexo
---
### 登录到GitHub,如果没有GitHub帐号，使用你的邮箱注册GitHub帐号：Build software better, together 点击GitHub中的New repository创建新仓库，仓库名应该为：用户名.http://github.io 这个用户名使用你的GitHub帐号名称代替，这是固定写法，比如我的仓库名为：

``` bash
$ hexo new "My New Post"
```

``` bash
$ git config --global user.name "fairytalefu"
$ git config --global user.email "fairytalefu@outlook.com"
$ ssh-keygen -t rsa -C "fairytalefu@outlook.com"
$ 
```

###  打开GitHub_Settings_keys 页面，新建new SSH Key
https://github.com/settings/keys
### 验证是否成功
```bash
$ ssh git@github.com
```

### 图床首选七牛云

