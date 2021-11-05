# Ethereum Multisignature Wallet
## 1.说明
本项目fork自https://github.com/gnosis/MultiSigWallet。
已经编译好了，开箱即用。
## 2.搭建环境
### 1）centos 7 系统
``` bash
yum install nginx -y
cd /etc/nginx/conf.d
vi multisigwallet.conf
```
编辑multisigwallet.conf，内容如下：
``` bash
server {
  listen 80;
  server_name wallet.xxxx.xxxx;
  root /data/web/multisigwallet;
  location / {
  }
 access_log /data/logs/nginx/multisigwallet.access.log main;
}
```
自行修改server_name 的内容，改成想要配置的访问域名。

### 2）ubuntu 系统
``` bash
apt install nginx -y
cd /etc/nginx/conf.d
vi multisigwallet.conf
```
内容跟centos7一样。

## 3.克隆代码
``` bash
mkdir /data/web/ -p
cd /data/web/
git clone https://github.com/xxxx/multisigwallet.git
```
## 4.启动nginx
``` bash
nginx
```