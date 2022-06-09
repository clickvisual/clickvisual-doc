# 开发环境构建
快速搭建本地开发环境

## 启动
fork 代码后，在项目根目录可以看到，以下两个文件，根据自己的硬件情况选择启动
- docker-compose.devops.yml
- docker-compose.devops.m1.yml

例如 mac m1 机器可以执行
>  docker-compose -f docker-compose.devops.m1.yml up

成功启动

![img.png](../../images/env.png)

## 运行本地开发代码

### 初始化
> go run ./api/main.go --config=./config/default.toml

![img_1.png](../../images/env-1.png)

完成数据库初始化之后，使用 clickvisual/clickvisual 登录

### 新增日志库
创建实例 
> tcp://127.0.0.1:9000?username=root&password=root&read_timeout=10&writer_timeout=10&debug=true

![img_3.png](../../images/env-3.png)

创建数据库

![img_2.png](../../images/env-2.png)

创建日志库
- kafka:9092
- ingress-stdout

![img_4.png](../../images/env-4.png)

### 测试数据生产

访问 [http://localhost:19003/](http://localhost:19003/)

![img.png](../../images/env-8.png)

![img_5.png](../../images/env-5.png)


### 前端开发

如果进行前端开发，需要进入 ui 目录，使用 yarn 启动

保证 target 指向后端服务即可

![img_6.png](../../images/env-6.png)

![img_7.png](../../images/env-7.png)

