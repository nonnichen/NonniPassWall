# NonniPassWall
 
简洁部署方案:

脚本修改自互联网
基于 Docker 容器架构的 Trojan-Go/VLESS/VMess-TCP/WS-TLS 分流部署&管理脚本
前置分流采用 TSP 进行 TLS，后端使用 Trojan-Go，V2Ray 容器，WatchTower，Portainer 维护组件，快速部署维护。


食用方法:

1. 安装 Wget:
Centos 7+
command -v wget >/dev/null 2>&1 || sudo yum -y install wget

Debian 9+ | Ubuntu 16+
command -v wget >/dev/null 2>&1 || sudo apt -y install wget

2. 执行脚本:
wget -N --no-check-certificate -q https://nonni.cn/s/NonniPassWall.sh && chmod +x NonniPassWall.sh && bash NonniPassWall.sh


配置文件:

WebSite：/home/wwwroot/nonnix/
TLS-Shunt-Proxy：/etc/tls-shunt-proxy/config.yaml
Trojan-Go：/etc/trojan-go/config.json
V2Ray：/etc/v2ray/config.json


Docker 访问 Portainer:

http://ServerDomainName:8858

如需解决端口占用
查看: netstat -anp | grep 80
结束: kill -9 pid


Support by Nonni
2020