# Swoft基础

> Author: Sylvie233
>
> Date: 23/2/9
>
> Point: 

[TOC]

## 基础介绍

### 项目目录

```
swoft:
	/app:
		/Boot:
			MyProcess.php:
		/Breaker:
		/Commands:
		/Controllers:
		/Exception:
		/Fallback:
		/Helper:
			Functions.php:
		/Lib:
		/Listener:
		/Middlewares:
		/Models:
			/Dao:
			/Data:
			/Entity:
			/Logic:
		/Pool:
		/Process:
			MyProcess.php:
		/Services:
		/Tasks:
		/WebSocket:
		Swoft.php:
	/bin:
		swoft:
	/config:
		/beans:
			base.php:
            console.php:
            log.php:
            service.php:	
		/properties:
			app.php:
			breaker.php:
			cache.php:
			db.php:
			provider.php:
			service.php:
		define.php:
		server.php:
	/public:
	/resources:
	/runtime:
	/test:
	/vendor:
	.env:
	.php_cs:
	.travis.yml:
	composer.json:
```



#### config/beans/base.php

```
[
	"serverDispatcher" => [
		"middlewares" => [ // 全局中间件
			
		]
	]
]
```



#### config/properties/cache.php

```
[
	"redis" => [
		"name",
		"uri",
		"db",
	]
]
```



#### config/properties/db.php

```
[
	"master" => [
		"name",
		"uri",
		"minActive",
		"maxActive",
		"maxWait",
		"timeout",
		"maxIdleTime",
		"maxWaitTime",
	],
	"slave" => []
]
```



### 开发者工具

`swoft/devtool`



### swoft

```
swoft:
	app:
		check:
		env:
    entity:
    	create:
	gen:
		controller:
	start:
```







## 核心内容

### 容器

#### 注解

```
注解：
	@After():
	@AfterReturning():
	@AfterThrowing():
	@Annotation:
	@Arguments:
	@Around():
	@Aspect():
	@Bean():
		name:
	@Before():
	@Column():
	@Command():
	@Controller():
		prefix:
	@Entity():
	@Example:
    @ExceptionHandler():
    @Handler():
    @Id():
	@Inject():
	@Listener():
	@Middleware():
		class:
	@Middlewares():
	@Options:
	@PointAnnotation():
	@PointBean():
	@PointExecution():
		include:
		exclude:
	@Process():
		boot:
		name:
	@RequestMapping():
		method:
		route:
	@Required():
	@Scheduled():
		cron:
	@ServerListener():
	@Table():
	@Target():
	@Task():
	@Usage:
	@view():
		layout:
		template:
	---
	@access
	@contact
	@document
	@license
	@link
	@method
	@package
	@param:
	@return:
	@throws:
	@uses:
	@var:
```





### 事件



### 中间件

```
MiddlewareInterface:
	process():
```



### 异常处理



### 模型

```
Model:
	batchInsert():
	count():
	deleteById():
	deleteOne():
	exist():
	fill():
	findAll():
	findById():
	findByIds():
	findOne():
	query():
		get():
		where():
	save():
	updateAll():
	updateOne():
        getResult():
```



### 任务



### 进程



### 命令



### AOP







## API

### swoft

```
swoft:
	\Swoft:
		\Bean:
			\Annotation:
			\Parser:
				AbstractParser:
			\Wrapper:
				AbstractWrapper:
			Collector:
			CollectorInterface:
		\Bootstrap:
			\Listeners:
				\Interfaces:
					WorkerStartInterface:	
					StartInterface:
             SwooleEvent:
             	ON_WORDER_START:
		\Core:
			RequestContext:
		\Db:
			Model:
			Query:
				table():
					andHaving():
					batchInsert():
					closeWhere():
					condition():
					counter():
					delete():
					get():
					groupBy():
					having():
					innerJoin():
                    insert():
                    limit():
                    max():
                    one():
                    openWhere():
                    orWhere():
                    update():
                    where():
                    whereIn():
		\Event:
			EventHandlerInterface:
		\Http:
			\Message:
				\Server:
					Request:
						file():
						header():
						input():
						post():
						query():
					Response:
						json():
						redirect():
						withAddedHeader():
			\Server:
				\Bean:
					\Annotation:
						Controller:
        \Process:
        	Process:
        \Redis:
        	Redis:
        		get():
        		lPop():
        		lPush():
        		set():
        \Task:
        	Task:
        		deliver():
        		deliverByProcess():
        App:
        	getBean():
        Server:
        Timer:
        	tick():
        trigger():
```































