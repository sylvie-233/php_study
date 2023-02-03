# Apache基础

> Author: Sylvie233
>
> Date: 23/1/12

[TOC]

## 基础介绍

安装目录

```
Apache:
	/bin:
		httpd: 启动命令
	/cgi-bin:
	/conf:
		httpd.conf
	/error:
	/htdocs:
	/icons:
	/include:
	/lib:
	/logs:
	/man:
	/manual:
	/modules:
	/modules:
```



### httpd

```
httpd:
	-k:
		install: 安装service
	-n: 名称
```



Apache Monitor可视化监控



### apachectl

```
apachectl:
	
```







## 核心内容

## 常用配置

配置文件：`httpd.conf`

```
ServerRoot "/xxx/xxx安装目录"
Listen 80
ServerAdmin xxx@xxx
ServerName xxx域名


LoadModule xxx_module modules/xxx.so	# 加载功能模块

<IfModule xxx_module>
</IfModule>
<IfModule unixd_module>					# 配置进程启动的用户和用户组
	User daemon
	Group daemon
</IfModule>
<IfModule dir_module>
	DirectoryIndex index.html			# 首页文件
</IfModule>



Document "/xxx/xxx网站根目录"
<Directory />
	AllowOverride none					# 是否读取目录中的.htaccess文件来修改设置的权限
	Require all denied					# 禁止所有请求访问资源
	Options Indexes FollowSymLinks		# 
</Directory>
<Directory "/xxx/xxx目录">
</Directory>



ErrorLog "logs/error.log"
LogLevel warn
<IfModule log_config_module>
	LogFormat "%h %l %u %t" common		# 自定义日志格式
</IfModule>
CustomLog "logs/access_log" common		# 引用日志格式


LoadModule php7_module "/xxx/php7apache2_4.dll"			# 整合php模块
AddType application/x-httpd-php .php .html .htm
PHPIniDir "/xxx"										# 指定php.ini配置文件目录


Include conf/extra/httpd-default.conf	# 引用其他配置文件
Timeout 300
KeepAlive On
KeepAliveTimeout 15
ServerTokens Prod						# 隐藏http响应中的Apache版本号
ServerSignature Off
HostnameLookups Off


Include conf/extra/httpd-mpm.conf	# 引用其他配置文件，Apache运行模式配置
PidFile logs/httpd.pid
<IfModule mpm_perfork_module>
	StartServers 5
	MinSpareServers 5
	MaxSpareServers 10
	MaxRequestWorkers 250
	MaxConnectionsPerChild 20000
</IfModule>


Include conf/extra/httpd-info.conf	# 引用其他配置文件，Apache状态页面
<Location /server-status>
	SetHandler server-status
	Require host xxx.com
	Require ip x.x.x.x
</Location>


Include conf/extra/httpd-vhosts.conf	# 引用其他配置文件，虚拟主机配置
<VirtualHost *:80>
	ServerName 虚拟主机域名
	ServerAddmin xxx@xxx
	DocumentRoot /xxx/xxx
	ErrorLog logs/error_log
	<Directory "/xxx/xxx目录">
        Options None
        AllowOverride None
        Require all granted
    </Directory>
</VirtualHost>


<IfModule proxy_fcgi_module>			# fastcig转发解析php
	<FilesMatch ".+\.php$">
		SetHandler "proxy:fcgi://127.0.0.1:9000"		# 绑定到fastcgi解析端口上
		# SetHandler "proxy:unix:/xxx/php7.4-fpm.sock"	# 绑定到socket文件上
	</FilesMatch>
</IfModule>
```

