---
title: Debian VPS常用设置
layout: post
tags:
  - debian
  - vps
category: it
---
## basic

``` bash
rm -rf /etc/localtime 
ln -s /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
apt update && apt upgrade -y
apt install vim nano htop curl unzip
cp /usr/share/vim/vim74/vimrc_example.vim .vimrc
vim /etc/ssh/sshd_config
wget https://raw.githubusercontent.com/scopatz/nanorc/master/install.sh -O- | sh
wget -qO- https://raw.githubusercontent.com/oooldking/script/master/superbench.sh | bash
wget -N --no-check-certificate https://raw.githubusercontent.com/FunctionClub/ZBench/master/ZBench.sh && bash ZBench.sh
wget -qO- bench.sh | bash
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/ssr.sh && chmod +x ssr.sh && bash ssr.sh
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/status.sh && chmod +x status.sh
bash <(curl -L -s https://install.direct/go.sh)
wget -N --no-check-certificate https://softs.fun/Bash/ocserv.sh && chmod +x ocserv.sh && bash ocserv.sh
curl https://raw.githubusercontent.com/linhua55/lkl_study/master/get-rinetd.sh | bash
```
## enable bbr
```bash
echo "tcp_bbr" >> /etc/modules-load.d/modules.conf
echo "net.core.default_qdisc=fq" >> /etc/sysctl.conf
echo "net.ipv4.tcp_congestion_control=bbr" >> /etc/sysctl.conf
sysctl -p
sysctl net.ipv4.tcp_available_congestion_control
sysctl net.ipv4.tcp_congestion_control
```
## add swap
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
## shadowsocks-libev
```bash
#debian8
sh -c 'printf "deb http://deb.debian.org/debian jessie-backports main\n" > /etc/apt/sources.list.d/jessie-backports.list'
sh -c 'printf "deb http://deb.debian.org/debian jessie-backports-sloppy main" >> /etc/apt/sources.list.d/jessie-backports.list'
apt update
apt -t jessie-backports-sloppy install shadowsocks-libev
#debian9
sudo sh -c 'printf "deb http://deb.debian.org/debian stretch-backports main" > /etc/apt/sources.list.d/stretch-backports.list'
sudo apt update
sudo apt -t stretch-backports install shadowsocks-libev
#ubuntu
sudo apt-get install software-properties-common -y
sudo add-apt-repository ppa:max-c-lv/shadowsocks-libev -y
sudo apt-get update
sudo apt install shadowsocks-libev
#config
{
    "server":["[::0]","0.0.0.0"],
    "server_port":9999,
    "password":"",
    "timeout":60,
    "method":"aes-256-gcm"
}
```
