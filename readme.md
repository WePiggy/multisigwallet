# Ethereum Multisignature Wallet
## 1. Description
This project is forked from https://github.com/gnosis/MultiSigWallet.
It is already compiled and ready to use out of the box.
## 2. Build environment
### 1) centos 7 system
``` bash
yum install nginx -y
cd /etc/nginx/conf.d
vi multisigwallet.conf
```
Edit multisigwallet.conf to read as follows
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
Change the contents of server_name to the access domain you want to configure.

### 2) ubuntu system
``` bash
apt install nginx -y
cd /etc/nginx/conf.d
vi multisigwallet.conf
```
The content is the same as centos7.

## 3. Clone the code
``` bash
mkdir /data/web/ -p
cd /data/web/
git clone https://github.com/xxxx/multisigwallet.git
```
## 4. Start nginx
``` bash
nginx
```

Translated with www.DeepL.com/Translator (free version)
