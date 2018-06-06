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



设置连接数到 5W

```
查看目前资源限制
ulimit -a

设置 open files 5W
ulimit -n 50000

```



websocket  router 采用 docker 安装   

```
install docker
curl https://raw.githubusercontent.com/rancher/install-docker/master/17.03.2.sh  | sh

run crossbar.io
docker run -p 8080:8080 crossbario/crossbar 
```



slow-io  基于node.js 构建  ip  149.28.138.20

```
install  node.js
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs

install pm2

启动 应用
pm2 

```



client  需要安装 node.js 和 ab 测试工具

```
instal node.j 同上 slow-io

install  ab 测试工具
apt install apache2-utils
```

