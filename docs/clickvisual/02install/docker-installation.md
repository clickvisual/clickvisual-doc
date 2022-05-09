# Docker 安装

ClickVisual Docker 镜像地址：https://hub.docker.com/r/sevennt/ClickVisual/tags

## Docker 启动配置
> https://github.com/shimohq/ClickVisual/tree/master/data/all-in-one/ClickVisual/config

你需要把你的配置里 [mysql] 改成你本地 MySQL 的配置。

## 使用 Docker 启动
> docker run --name ClickVisual -e EGO_CONFIG_PATH=/ClickVisual/config/docker.toml -e EGO_LOG_WRITER=stderr -p 19001:19001 -d sevennt/ClickVisual:master -v ./config:/ClickVisual/config

需要把配置挂载到 docker 容器内

## 使用 Docker-Compose 命令
```
version: "3"
services:
ClickVisual:
image: sevennt/ClickVisual:master
container_name: ClickVisual
environment:
EGO_CONFIG_PATH: /ClickVisual/config/docker.toml
EGO_LOG_WRITER: stderr
ports:
- "19001:19001"
restart: always
volumes:
- ./config:/ClickVisual/config
command: [ '/bin/sh', '-c', './bin/ClickVisual' ]<br/>
```
需要把配置挂载到 docker 容器内

最后访问 http://localhost:19001



