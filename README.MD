5台独立服务器

* websocket router
* slow-io
* client
* node-server
* php-server



服务器软硬件配置参考

```
vultr 新加坡机房 VC2 实例
OS ubuntu 16.04 64位
CPU 6核
内存 16384GB
```



websocket  router 采用 docker 安装   

```
install docker
curl https://raw.githubusercontent.com/rancher/install-docker/master/17.03.2.sh  | sh

run crossbar.io
docker run -p 8080:8080 crossbario/crossbar 
```



slow-io  基于node.js 构建

```
install  node.js
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs

```



client  需要安装 node.js 和 ab 测试工具

```
instal node.j 同上 slow-io

install  ab 测试工具
apt install apache2-utils
```

