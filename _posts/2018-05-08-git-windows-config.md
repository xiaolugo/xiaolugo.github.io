---
title: git windows配置
layout: post
tags:
  - git
category: linux
---
git config --global user.name "demo" 设置你的用户名
git config --global user.email "demo@qq.com" 设置你的邮箱
ssh-keygen -t rsa -C “demo@qq.com 生成密钥
将id_rsa.pub里的内容复制出来粘贴到github个人中心的账户设置的ssh key里面
ssh -T git@github.com测试ssh keys是否设置成功
