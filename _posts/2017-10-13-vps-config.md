---
layout: post
title: vps quick config
date: '2017-10-13 12:34:25 +0800'
description: Set up vps to cross the GFW quickly.
tags: vps
categories:
  - it
---

# SSR
```bash
wget -N --no-check-certificate https://softs.fun/Bash/ssr.sh && chmod +x ssr.sh && bash ssr.sh
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
wget -N --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh && chmod +x bbr.sh && bash bbr.sh
```

# UML BBR
```bash
wget --no-check-certificate https://github.com/91yun/uml/raw/master/lkl/install.sh && bash install.sh
```

# 91test
```bash
wget -N --no-check-certificate https://raw.githubusercontent.com/91yun/91yuntest/master/test_91yun.sh && bash test_91yun.sh
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

# superspeed
```bash
wget https://raw.githubusercontent.com/oooldking/script/master/superspeed.sh && chmod +x superspeed.sh && ./superspeed.sh
```

# bench
```bash
wget -qO- bench.sh | bash
```

# ss libev
```bash
sudo apt-get install software-properties-common -y
sudo add-apt-repository ppa:max-c-lv/shadowsocks-libev
sudo apt-get update
sudo apt install shadowsocks-libev
```

# nano
```bash
wget https://raw.githubusercontent.com/scopatz/nanorc/master/install.sh -O- | sh
```

# Other
