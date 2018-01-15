---
title: 部署vps一件脚本
layout: post
tags:
  - vps
category: it
---
# Basic
```bash
passwd
rm -rf /etc/localtime 
ln -s /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
apt update && apt upgrade -y
apt install vim nano htop curl unzip screen
cp /usr/share/vim/vim74/vimrc_example.vim .vimrc
vim /etc/ssh/sshd_config
wget https://raw.githubusercontent.com/scopatz/nanorc/master/install.sh -O- | sh
```
# Bench
```bash
wget -qO- https://raw.githubusercontent.com/oooldking/script/master/superbench.sh | bash
wget -qO- bench.sh | bash
```
# LNMP
```bash
screen -S lnmp
wget -c http://soft.vpser.net/lnmp/lnmp1.4.tar.gz && tar zxf lnmp1.4.tar.gz && cd lnmp1.4 && ./install.sh 
```
# SSR
```bash
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/ssr.sh && chmod +x ssr.sh && bash ssr.sh
```
# Status
```bash
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/status.sh && chmod +x status.sh
```
# V2ray
```bash
bash <(curl -L -s https://install.direct/go.sh)
```
# Goflyaway
```bash
wget -N --no-check-certificate https://softs.fun/Bash/goflyway.sh && chmod +x goflyway.sh && bash goflyway.sh
```
# BBR
```bash
wget --no-check-certificate https://github.com/91yun/uml/raw/master/lkl/install.sh && bash install.sh
curl https://raw.githubusercontent.com/linhua55/lkl_study/master/get-rinetd.sh | bash
```
# Adbyby
```bash
wget -N --no-check-certificate https://softs.fun/Bash/adbyby.sh && chmod +x adbyby.sh && bash adbyby.sh
```
# Ocserv
```bash
wget -N --no-check-certificate https://softs.fun/Bash/ocserv.sh && chmod +x ocserv.sh && bash ocserv.sh
```
# Besttrace
```bash
wget -N --no-check-certificate https://softs.fun/Other/besttrace.tar.gz
tar -xzf besttrace.tar.gz && cd besttrace && chmod +x *
./besttrace -q 1
```


