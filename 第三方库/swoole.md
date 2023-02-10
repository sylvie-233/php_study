# Swoole基础

> Author: Sylvie233
>
> Date: 23/2/9
>
> Point: 

[TOC]

## 基础介绍

基于事件的高性能异步、协程并行网络通信引擎









## 核心内容



### 协程



### 通道







## API

### swoole

```
swoole:
	\Swoole:
		\Coroutine:
			\Http:
				Client:
			\Http2:
			Channel:
			Redis:
				connect():
				get():
		\Http:
			Request:
				fd:
				get():
			Response:
				cookie():
				end():
			Server:
				on():
					request:
					workerStart:
				set():
					document_root:
                	enable_static_handler:
		\WebSocket:
			Frame:
				data:
				fd:
			Server:
				on():
					Close:
					Finish:
					Message:
					Open:
					task:
				push():
				set():
					task_worker_num:
				start():
                task():
        Client:
        	connect():
        	send():
        Event:
        Process:
        	exec():
        	read():
        	start():
        	wait():
        	write():
        Runtime:
        Server:
        	on():
        		Close:
        		Connect:
        		Receive:
            send():
            set():
            	max_request:
            	workder_num:
            start():
        Table: 内存表
        	column():
        	create():
        	decr():
        	del():
        	exists():
        	get():
        	incr():
        	set():
        Timer:
        	after():
        	tick():
	
	go(): 创建协程
	swoole_client():
	swoole_http_server():
	swoole_server():
```



















