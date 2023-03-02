# 科学上网：VPS 搭建 X-UI 面板

## 一、安装更新运行环境

### 1、Debian/Ubuntu系统执行以下命令：
    
    apt update -y && apt install -y curl && apt install -y socat
     
### 2、CentOS系统执行以下命令：

    yum update -y && yum update -y && yum install -y socat


### 二、获取VPS的root权限，随意更改root密码的一键脚本，已测试EUserv德鸡，Hax IPV6，甲骨文oracle、谷歌云gpc、IBM Linux one、亚马逊云azurz等
获取Root权限，可改root密码的一键脚本
甬哥侃侃侃ygkkk一键脚本 ：

    wget -N https://gitlab.com/rwkgyg/vpsroot/raw/main/root.sh && bash root.sh

### 三、安装&升级x-ui面板一键脚本
###
### 原版
    bash <(curl -Ls https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh)

### 甬哥侃侃侃ygkkk ：

    wget -N https://gitlab.com/rwkgyg/x-ui-yg/raw/main/install.sh && bash install.sh

### ubuntu开放所有端口

    iptables -P INPUT ACCEPT
###
    iptables -P FORWARD ACCEPT
###
    iptables -P OUTPUT ACCEPT
###
    iptables -F
###
    iptables-save
###
### 如果想持续化规则：使用iptables-persistent
永久打开需要的端口（重启也生效）
首先安装

    iptables-persistent
###
    apt-get install iptables-persistent

### 永久保存规则

    netfilter-persistent save
###
    netfilter-persistent reload
###
