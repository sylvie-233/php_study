# PHP基础

> Author: Sylvie233
>
> Date: 23/1/12
>
> Point: P58

[TOC]

## 基础介绍



### php

```
php:
	
```





### composer

```
composer:
	-d:
	--profile: 查看耗时和内存使用情况
	-q:
	-V:
	-v: 提示信息
    -vvv: 详细信息
    archive:
    	--file:
    	--format:
	browse:
		--homepage:
		--show:
	check-paltform-reqs: 包平台检测
    config:
        -g:
        -l:
        --unset:
    create-project:
    clear-cache:
    diagnose:
    dump-autoload: 根据json配置的autoload更新autoload_psr4.php文件
        --optimize:
    exec:
    global: 全局命令
    init: 初始化json
    	-n:
    install:
    	--no-dev:
    licenses:
    	--format:
    list:
    remove:
    require:
    run-script:
    search:
    	--only-name:
    	--type:
    self-update: composer更新
    	-r:
    show:
    	--all:
    	--direct: 直系依赖
    	--outdate: 列出新版本可用包（检测更新）
    	--tree:
    status:
    	--verbose:
    update:
    validate: 校验json格式
```



#### composer.json

```
{
	author: [""],
	authors: [
		{
			name:
			email:
			homepage:
			role:
		}
	],
	autoload: {
		files: [],
		"psr-4": {
			"XXX\\": "src/XXX"
        },
		"psr-0": { // 命名空间指定的目录是父级目录（命名空间与当前目录同名，下划线目录拆分多一级）
		
		},
        classmap: { // 生成classmap的php文件列表
		
        },
        "exclude-from-classmap": []
	},
	autoload-dev: {
	
	},
	config: {
        htaccess-protect:
		process-timeout:
		sort-packages:
		use-include-path:
	}
    conflict: { // 包版本禁止
    
    },
	description: "",
	extra: {
		branch-alias:
	},
	homepage: "项目网站主页",
	keywords: [搜索关键字],
	license: "",
	prefer-stable: true,
	provide: { // 登记包可能的依赖
		
	},
	minimum-stability: "stable|dev|rc|"
	name: "",
	replace: {
	
	},
	repositories: {
		packagist: {
			type: composer
			url:
		}
	}
	require: {
		"php": "^5.5 || ^7.0",
	}
	require-dev: {
		
	}
	scripts: {
		xxx: []
	}
	suggest: {
		
	},
	support: {
		email:
		source:
		issues:
	}
	time: "发布时间	",
	type: library|project|metapackage|composer-plugin,
	version: "",
}
```





packagist.org包管理网站

自动加载原理：

```
require __DIR . "/vendor/autoload.php"
	$loader:
		addPsr4(): 手动添加映射
```



PSR-4自动加载规范

PSR-0自动加载规范





vendor目录

```
vendor:
	/composer:
		autoload_classmap.php:
		autoload_namespaces.php:
		autoload_psr4.php:
		autoload_real.php:
		autoload_static.php:
		ClassLoader.php:
		installed.json:
	/xxx包:
	autoload.php: 自动加载
```



##### autoload_psr4.php

```php
$vendorDir = dirname(dirname(__FILE__))
$baseDir = dirname($vendorDir)
    
return array(
	"Monolog\\" => array($vendorDir . "/monolog/monolog/src/Monolog")
)
```



##### classmap.php

缓存类映射路径

```
$vendorDir = dirname(dirname(__FILE__))
$baseDir = dirname($vendorDir)
    
return array()
```





































安装目录：

```
php:
	/dev:
	/ext:
	/extras:
	/lib:
	/sasl2:
	php.ini-development:
	php.ini-production:
	php7apache2_4.dll:
```



### 配置文件

配置文件：`php.ini`

```ini
[PHP]

```



## 核心内容

### 预定义变量

```
$GLOBALS — 引用全局作用域中可用的全部变量
$_SERVER — 服务器和执行环境信息
$_GET — HTTP GET 变量
$_POST — HTTP POST 变量
$_FILES — HTTP 文件上传变量
$_REQUEST — HTTP Request 变量
$_SESSION — Session 变量
$_ENV — 环境变量
$_COOKIE — HTTP Cookies
$php_errormsg — 前一个错误信息
$HTTP_RAW_POST_DATA — 原生POST数据
$http_response_header — HTTP 响应头
$argc — 传递给脚本的参数数目
$argv — 传递给脚本的参数数组

```





### 流程控制

```
if
else
elseif/else if
while
do-while
for
foreach
break
continue
switch
declare
return
require
include
require_once
include_once
goto
```





## 标准库

### 1.影响 PHP 行为的扩展

### 2.音频格式操作

### 3.身份认证服务

### 4.针对命令行的扩展

### 5.压缩与归档扩展

### 6.信用卡处理

### 7.加密扩展

### 8.数据库扩展

### 9.日期与时间相关扩展

### 10.文件系统相关扩展

### 11.国际化与字符编码支持•Enchant — Enchant spelling library

### 12.图像生成和处理

### 13.邮件相关扩展

### 14.数学扩展

### 15.非文本内容的 MIME 输出

### 16.进程控制扩展

### 17.其它基本扩展

### 18.其它服务

### 19.搜索引擎扩展

### 20.针对服务器的扩展

### 21.Session 扩展

### 22.文本处理

#### 字符串

##### strlen

##### strtoupper





### 23.变量与类型相关扩展

### 24.Web 服务

### 25.Windows 专用扩展

### 26.XML 操作

### 27.图形用户界面(GUI) 扩展