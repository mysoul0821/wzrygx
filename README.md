首先你需要买一台服务器，不限于腾讯 阿里 京东 或者其他小厂商的 推荐买腾讯云  新人有试用和38元一年的优惠

我拿一台闲置服务器来演示
服务器的配置很低，几个人用足够了，尽量买那种一年就几十块的服务器

CPU：2核
内存：2GB
带宽：3Mbps

首先购买服务器后安装centos7 系统

第二步用远程服务器连接工具 xshell5 工具来连接

第三步安装宝塔面板

if [ -f /usr/bin/curl ];then curl -sSO https://download.bt.cn/install/install_panel.sh;else wget -O install_panel.sh https://download.bt.cn/install/install_panel.sh;fi;bash install_panel.sh ssl251104

输入y 回车

等待安装完成

安装完成后会出现后台面板和登录密码

 【云服务器】请在安全组放行 33212 端口
 外网ipv4面板地址: https://117.72.112.31:33212/b793a469
 内网面板地址:     https://172.16.0.9:33212/b793a469
 username: 11725433
 password: c999060d

我这台是安装过的 我重新安装 这些都不用看 因为你们新主机没有这些东西

下面到应用商场搜索安装

Nginx

PHP-8.2

java项目-添加项目-添加jdk信息-jdk1.8.0_371	

下面就等这3个依赖安装好就可以上传源码到服务器了


添加站点-域名输入你的服务器IP

根目录 点进去 点上传文件 上传源码  双击解压  所有文件必须放到网站根目录下


然后点左侧网站-java项目-添加项目

项目路径
/www/wwwroot/117.72.112.31/home-server-0.0.1-SNAPSHOT.jar

/www/server/java/jdk1.8.0_371/bin/java -jar  -Xmx1024M -Xms256M /www/wwwroot/117.72.112.31/home-server-0.0.1-SNAPSHOT.jar

点取消 只要项目启动命令

其他项目-添加项目-项目执行文件/www/wwwroot/117.72.112.31/home-server-0.0.1-SNAPSHOT.jar

项目端口8888

显示运行中就可以了


只要上面的时间前面的点事蓝色的就说明搭建成功了
