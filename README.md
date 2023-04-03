# NonniPassWall
 
简洁部署方案:

脚本修改自互联网。</br>
基于 Docker 容器架构的 Trojan-Go/VLESS/VMess-TCP/WS-TLS 分流部署&管理脚本。</br>
前置分流采用 TSP 进行 TLS，后端使用 Trojan-Go，V2Ray 容器，WatchTower，Portainer 维护组件，快速部署维护。</br>


食用方法: </br>

1. 安装 Wget: </br>
Centos 7+ </br>
command -v wget >/dev/null 2>&1 || sudo yum -y install wget

Debian 9+ | Ubuntu 16+ </br>
command -v wget >/dev/null 2>&1 || sudo apt -y install wget

2. 执行脚本: </br>
wget -N --no-check-certificate -q  https://raw.githubusercontent.com/nonnichen/NonniPassWall/main/NonniPassWall.sh && chmod +x NonniPassWall.sh && bash NonniPassWall.sh


配置文件: </br>

WebSite：/home/wwwroot/nonnix/ </br>
TLS-Shunt-Proxy：/etc/tls-shunt-proxy/config.yaml </br>
Trojan-Go：/etc/trojan-go/config.json </br>
V2Ray：/etc/v2ray/config.json </br>

Docker 访问 Portainer:</br>
http://ServerDomainName:8858
</br>
如需解决端口占用:</br>
查看: netstat -anp | grep 80 </br>
结束: kill -9 pid </br>
</br>

Support by Nonni</br>
2020