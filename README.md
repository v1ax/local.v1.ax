# local.v1.ax
### 本项目可解决本机部署的web项目不方便进行https调试的问题

因无法在 127.0.0.1 或 localhost部署CA证书,导致本地项目https访问困难

解决原理:

  1.本域名 [local.v1.ax](https://tool.chinaz.com/dns/local.v1.ax)已永久指向 127.0.0.1 
  
  2.[下载](https://v1.ax/local)cer_download目录下提供的证书和私钥tar包,解压并部署到项目中.
  
  3.使用 https://local.v1.ax 访问即可.

  > 证书有效期3个月,到期后自动更新

-----------------------------------
新增 [xip.v1.ax]() 匹配返回任意指定IP：

> 不提供通配证书下载,需根本下方规则,使用[HTTP-01 质询](https://letsencrypt.org/docs/challenge-types/#http-01-challenge)自行申请

|主机名/URL|IP地址|说明|
|---|---|---|
|[https://52.0.56.137.xip.v1.ax](https://tool.chinaz.com/dns/52.0.56.137.xip.v1.ax)	|52.0.56.137	|点分隔符|
|[https://52-0-56-137.xip.v1.ax](https://tool.chinaz.com/dns/52-0-56-137.xip.v1.ax)	|52.0.56.137	|破折号分隔符|
|[www.192.168.0.1.xip.v1.ax](https://tool.chinaz.com/dns/www.192.168.0.1.xip.v1.ax)	|192.168.0.1	|子域名|
|[www.192-168-0-1.xip.v1.ax](https://tool.chinaz.com/dns/www.192-168-0-1.xip.v1.ax)	|192.168.0.1	|子域名 + 破折号|
|[https://www-78-46-204-247.xip.v1.ax](https://tool.chinaz.com/dns/www-78-46-204-247.xip.v1.ax)	|78.46.204.247	|dash 前缀|
|[https://--1.xip.v1.ax](https://www.itdog.cn/ping_ipv6/--1.xip.v1.ax)	|::1	|IPv6 — 始终使用破折号，不要使用点|
|[https://2a01-4f8-c17-b8f--2.xip.v1.ax](https://www.itdog.cn/ping_ipv6/2a01-4f8-c17-b8f--2.xip.v1.ax)	|2a01:4f8:c17:b8f::2	|IPv6 — 始终使用破折号，不要使用点|

> 附[ACME HTTP-0申请证书说明](https://github.com/acmesh-official/acme.sh/wiki/%E8%AF%B4%E6%98%8E#1-http-%E6%96%B9%E5%BC%8F%E9%9C%80%E8%A6%81%E5%9C%A8%E4%BD%A0%E7%9A%84%E7%BD%91%E7%AB%99%E6%A0%B9%E7%9B%AE%E5%BD%95%E4%B8%8B%E6%94%BE%E7%BD%AE%E4%B8%80%E4%B8%AA%E6%96%87%E4%BB%B6-%E6%9D%A5%E9%AA%8C%E8%AF%81%E4%BD%A0%E7%9A%84%E5%9F%9F%E5%90%8D%E6%89%80%E6%9C%89%E6%9D%83%E5%AE%8C%E6%88%90%E9%AA%8C%E8%AF%81-%E7%84%B6%E5%90%8E%E5%B0%B1%E5%8F%AF%E4%BB%A5%E7%94%9F%E6%88%90%E8%AF%81%E4%B9%A6%E4%BA%86)
------------------------------------------------------
