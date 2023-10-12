#### **Nginx** **的安装**

**到** **nginx** **官网下载软件**  http://nginx.org/



#### **安装** **pcre** **依赖**

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



#### 查看开放的端口号

**firewall-cmd --list-all**



#### 设置开放的端口号

**firewall-cmd --add-service=http –permanent**

**firewall-cmd --add-port=80/tcp --permanent**



#### 重启防火墙

**firewall-cmd –reload**