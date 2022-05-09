# 二进制安装

二进制安装支持四种架构：darwin-amd64、linux-amd64、darwin-arm64、linux-arm64。


## Mac AMD64 架构

```
# 获取最新版本
latest=$(curl -sL https://api.github.com/repos/shimohq/mogo/releases/latest | grep  ".tag_name" | sed -E 's/.*"([^"]+)".*/\1/')

# MacOS amd64系统
wget "https://github.com/shimohq/mogo/releases/download/${latest}/mogo-${latest}-darwin-amd64.tar.gz" -O mogo-${latest}.tar.gz
```

![img.png](../../images/binary-download.png)

## Linux AMD64 架构
```
# 获取最新版本
latest=$(curl -sL https://api.github.com/repos/shimohq/mogo/releases/latest | grep  ".tag_name" | sed -E 's/.*"([^"]+)".*/\1/')

# Linux amd64系统
wget "https://github.com/shimohq/mogo/releases/download/${latest}/mogo-${latest}-linux-amd64.tar.gz" -O mogo-${latest}.tar.gz
```
## Mac ARM64 架构
```
# 获取最新版本
latest=$(curl -sL https://api.github.com/repos/shimohq/mogo/releases/latest | grep  ".tag_name" | sed -E 's/.*"([^"]+)".*/\1/')

# Mac arm64系统
wget "https://github.com/shimohq/mogo/releases/download/${latest}/mogo-${latest}-mac-arm64.tar.gz" -O mogo-${latest}.tar.gz
```

## Linux ARM64 架构
```
# 获取最新版本
latest=$(curl -sL https://api.github.com/repos/shimohq/mogo/releases/latest | grep  ".tag_name" | sed -E 's/.*"([^"]+)".*/\1/')

# Linux arm64系统
wget "https://github.com/shimohq/mogo/releases/download/${latest}/mogo-${latest}-linux-arm64.tar.gz" -O mogo-${latest}.tar.gz
```

## 启动 Mogo
```
# 解压压缩包
mkdir -p ./mogo-${latest} && tar -zxvf mogo-${latest}.tar.gz -C ./mogo-${latest}

# 修改配置文件 config/default.toml，将 MySQL、Redis 等配置改成你自己的配置。
# 修改完配置文件后，使用如下指令运行 mogo
cd ./mogo-${latest} && ./mogo -config config/default.toml

# 访问 http://localhost:19001
# login username: shimo
# login password: shimo
```