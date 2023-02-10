# Laravel基础

> Author: Sylvie233
>
> Date: 23/1/30
>
> Point: 

[TOC]

## 基础介绍

### 项目目录

```
laravel:
	/app:
		/Console:
			/Commands:
			Kernel.php:
		/Events:
		/Exceptions:
		/Http:
			/Controllers:
				/Auth:
				Controller.php:
			/Middleware:
			/Requests:
			Kernel.php:
		/Jobs:
		/Listeners:
		/Providers:
		User.php:
	/bootstrap:
		/cache:
		app.php:
		autoload.php:
	/config:
		app.php:
		auth.php:
		broadcasting.php:
		cache.php:
		compile.php:
		database.php:
		filesystems.php:
		mail.php:
		queue.php:
		services.php:
		session.php:
		view.php:
	/database:
		/factories:
			ModelFactory.php:
		/migrations:
		/seeds:
			DatabaseSeeder.php:
	/public:
		index.php:
		.htaccess:
		web.config:
	/resources:
		/assets:
		/lang:
		/views:
			welcom.blade.php:
	/routes:
		api.php:
		channels.php:
		console.php:
		web.php:
	/storage:
		/app:
		/framework:
		/logs:
	/tests:
	/vendor:
	.env
	artisan:
	composer.json:
	log.txt:
	package.json:
	phpunit.xml:
	server.php:
```



#### .env

```
DB_USERNAME
DB_PASSWORD
```



#### app/Http/Kernel.php

```
:
	routeMiddleware: []
```







### artisan

```
artisan:
	make:
		contoller:
		model:
```





## 核心内容

### 模板

```
{{ var }}

{!! html !!}

内置函数:
	{{
		asset():
		csrf_field():
		csrf_token():
		env():
		url():
	}}

@extends()

@foreach($list as $it)
@endforeach

@if()
@endif

@include()

@section()
@endsection
```





### 控制器



### 路由

```
Route:
	current():
		getActionName():
	get():
	group():
	post():
	resource():
```





### 模型

```
Model:
	create():
	delete():
	find():
	get():
	update():
```



### 中间件

```
Middleware:
	handle():
```





### 存储













## API

### laravel

```
laravel:
	\Illuminate:
		\Database:
			\EEloquent:
				Model:
					fillable:
					guarded:
					primaryKey:
					table:
					timestamps:
					belongsToMany():
					create():
					decrement():
					delete():
					destory():
					find():
					first():
					orderBy():
					paginate():
					save():
					where():
		\Http:
			Request:
				all():
				except():
				file():
					getClientMimeType():
					getClientOriginalExtension():
					getClientOriginalName():
					getRealPath():
					isValid():
					move():
            Response:
            	json():
        \Support:
        	\Facades:
        		Crypt:
        			decrypt():
        			encrypt():
        		Hash:
        			check():
        			make():
        		Validator:
        			fails():
        			make():
            ServiceProvider:
            	boot():
	back():
	compact():
	dd():
	public_path():
	redirect():
		with():
		withErrors():
		withInput():
    session():
    	flush():
	url():
	view():
		with():
```































