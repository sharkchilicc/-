# 科学上网：VPS 搭建 X-UI 面板

## 一、安装更新运行环境

### 1、Debian/Ubuntu系统执行以下命令：
    
    apt update -y && apt install -y curl && apt install -y socat
     
### 2、CentOS系统执行以下命令：

    yum update -y && yum update -y && yum install -y socat


## 二、获取VPS的root权限，随意更改root密码的一键脚本，已测试EUserv德鸡，Hax IPV6，甲骨文oracle、谷歌云gpc、IBM Linux one、亚马逊云azurz等
获取Root权限，可改root密码的一键脚本
一键脚本

    wget -N https://gitlab.com/rwkgyg/vpsroot/raw/main/root.sh && bash root.sh

