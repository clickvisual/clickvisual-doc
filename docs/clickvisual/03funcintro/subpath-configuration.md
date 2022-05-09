# 子路径配置

`可用版本 >= 0.2.2`

需要修改两个配置：导入环境变量，重新编译前端；后端服务启动配置修改。

假设需要支持http://localhost:19001/mogo/这个子路径

1. 首先导入环境变量，重新编译前端，可以在项目根目录执行 make build.ui build.dist

> export PUBLIC_PATH=/mogo/

2. 完成前端编译后进行后端编译，执行make build.api

顺利完成以上两个步骤后，会在 ./bin 文件夹得到编译好的二进制文件，前端文件已经被打包到二进制文件



修改服务启动配置：
- serveFromSubPath 配置为 true
- rootURL 子路径配置

``` 
[app]
serveFromSubPath = true
rootURL = "http://localhost:19001/mogo/"
```

此时目录结构如下图所示，执行./bin/mogo --config=./config/default.toml 启动服务即可

![img.png](../../images/config-tree.png)