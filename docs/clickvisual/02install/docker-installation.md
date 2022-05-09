# Docker 安装

Mogo Docker 镜像地址：https://hub.docker.com/r/sevennt/mogo/tags

## Docker 启动配置
> https://github.com/shimohq/mogo/tree/master/data/all-in-one/mogo/config

你需要把你的配置里 [mysql] 改成你本地 MySQL 的配置。

## 使用 Docker 启动
> docker run --name mogo -e EGO_CONFIG_PATH=/mogo/config/docker.toml -e EGO_LOG_WRITER=stderr -p 19001:19001 -d sevennt/mogo:master -v ./config:/mogo/config

需要把配置挂载到 docker 容器内

## 使用 Docker-Compose 命令
```
version: "3"
services:
mogo:
image: sevennt/mogo:master
container_name: mogo
environment:
EGO_CONFIG_PATH: /mogo/config/docker.toml
EGO_LOG_WRITER: stderr
ports:
- "19001:19001"
restart: always
volumes:
- ./config:/mogo/config
command: [ '/bin/sh', '-c', './bin/mogo' ]<br/>
```
需要把配置挂载到 docker 容器内

最后访问 http://localhost:19001



