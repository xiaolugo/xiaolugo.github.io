---
title: CentOS 7 配置防火墙
layout: post
tags:
  - centos
category: it
---
# 讨厌的firewalld，你懂的。
```bash
# allow port
firewall-cmd --zone=public --add-port=9000/tcp --permanent
firewall-cmd --reload
firewall-cmd --list-all
firewall-cmd --state
# Disable firewall
systemctl disable firewalld
systemctl stop firewalld
systemctl status firewalld
# Enable firewall
systemctl enable firewalld
systemctl start firewalld
systemctl status firewalld
```
