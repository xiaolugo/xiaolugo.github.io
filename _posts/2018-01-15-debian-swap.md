---
title: Ubuntu/Debian添加SWAP
layout: post
tags:
  - vps
category: it
---
```bash
fallocate -l 1G /swapfile
chmod 600 /swapfile
mkswap /swapfile
swapon /swapfile
swapon -s
echo "/swapfile none swap sw 0 0" >> /etc/fstab
nano /etc/fstab
/swapfile none swap sw 0 0
```