#### **Nginx** **的安装**

**到** **nginx** **官网下载软件**  http://nginx.org/



##### **安装** **pcre** **依赖**

**第一步 联网下载** **pcre** **压缩文件依赖**

**wget http://downloads.sourceforge.net/project/pcre/pcre/8.37/pcre-8.37.tar.gz**

**第二步 解压压缩文件**

**使用命令** **tar –xvf pcre-8.37.tar.gz**

**第三步****./configure** **完成后，回到** **pcre** **目录下执行** **make****，最后执行** **make install**



**安装** **openssl** **、****zlib** **、** **gcc** **依赖**

**yum -y install make zlib zlib-devel gcc-c++ libtool openssl openssl-devel**



***** **使用命令解压**

*** ./configure**

*** make && make install**

**进入目录** **/usr/local/nginx/sbin/nginx** **启动服务**



**在** **windows** **系统中访问** **linux** **中** **nginx**，默认不能访问的，因为防火墙问题

- 关闭防火墙

- 开放访问的端口号，80 **端口**



##### 查看开放的端口号

**firewall-cmd --list-all**



##### 设置开放的端口号

**firewall-cmd --add-service=http –permanent**

**firewall-cmd --add-port=80/tcp --permanent**



##### 重启防火墙

**firewall-cmd –reload**





#### **Nginx** **的常用的命令**

- **进入** **nginx** **目录中**  **cd /usr/local/nginx/sbin**
- **查看** **nginx** **版本号** **./nginx -v**
- **启动** **nginx ./nginx**
- **停止nginx  ./nginx -s stop**
- **重新加载 nginx  ./nginx -s reload**





#### nginx的配置文件

- **nginx** **配置文件位置 ** **cd /usr/local/nginx/conf/nginx.conf**
- **配置文件中的内容**

**包含三部分内容**

**全局块：配置服务器整体运行的配置指令****

**比如 worker_processes 1;****处理并发数的配置**



**events块：影响 Nginx 服务器与用户的网络连接**

**比如 worker_connections 1024; 支持的最大连接数为 1024**



**http 块**

**还包含两部分：**

**http 全局块**

**server 块**