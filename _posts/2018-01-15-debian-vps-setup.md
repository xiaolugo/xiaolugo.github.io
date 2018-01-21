---
title: Debian VPS常用设置
layout: post
tags:
  - debian
  - vps
category: it
---
Debian VPS的一些常用设置及脚本。
## enable swap
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
<!-- more -->

## enable bbr on debian 9
```bash
echo "net.core.default_qdisc=fq" >> /etc/sysctl.conf
echo "net.ipv4.tcp_congestion_control=bbr" >> /etc/sysctl.conf
sysctl -p
sysctl net.ipv4.tcp_available_congestion_control
lsmod | grep bbr

sed -i '/net\.core\.default_qdisc=fq/d' /etc/sysctl.conf
sed -i '/net\.ipv4\.tcp_congestion_control=bbr/d' /etc/sysctl.conf
sysctl -p
```