# local.v1.ax
### 本项目可解决本机部署的web项目不方便进行https调试的问题

因无法在 127.0.0.1 或 localhost部署CA证书,导致本地项目https访问困难

解决原理:

  1.本域名 [local.v1.ax](https://tool.chinaz.com/dns/local.v1.ax)已永久指向 127.0.0.1 
  
  2.[下载](https://v1.ax/local)cer_download目录下提供的证书和私钥tar包,解压并部署到项目中.
  
  3.使用 https://local.v1.ax 访问即可.

  > 证书有效期3个月,到期后自动更新
