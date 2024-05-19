## 为什么访问服务器地址就能访问到项目  --配置一些东西

nginx  是一款轻量级的web服务器、反向代理服务器
能帮助我的服务器访 问到尚硅谷的服务器


## nginx配置：
1. xshell进入根目录下的etc
2. 进入etc目录下有一个nginx目录
3. 如果要安装nginx yum install nginx
4. 安装完后，找到nginx.conf文件 配置
5. vim nginx.conf 编辑
6. 编辑如下两项
(1)location / {
     root  /root/jch/www/shangpinghui/dist;
     index index.html;
     try_files $uri/ /index.html;
 }
(2) location /api {
    proxy_pass http://gmall-h5-api.atguigu.cn
}
6. !! nginx服务器跑起来
service nginx start