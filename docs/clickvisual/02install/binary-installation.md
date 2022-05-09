# 二进制安装

二进制安装支持四种架构：darwin-amd64、linux-amd64、darwin-arm64、linux-arm64。


## Mac AMD64 架构

```
# 获取最新版本
latest=$(curl -sL https://api.github.com/repos/shimohq/ClickVisual/releases/latest | grep  ".tag_name" | sed -E 's/.*"([^"]+)".*/\1/')

# MacOS amd64系统
wget "https://github.com/shimohq/ClickVisual/releases/download/${latest}/ClickVisual-${latest}-darwin-amd64.tar.gz" -O ClickVisual-${latest}.tar.gz
```

![img.png](../../images/binary-download.png)

## Linux AMD64 架构
```
# 获取最新版本
latest=$(curl -sL https://api.github.com/repos/shimohq/ClickVisual/releases/latest | grep  ".tag_name" | sed -E 's/.*"([^"]+)".*/\1/')

# Linux amd64系统
wget "https://github.com/shimohq/ClickVisual/releases/download/${latest}/ClickVisual-${latest}-linux-amd64.tar.gz" -O ClickVisual-${latest}.tar.gz
```
## Mac ARM64 架构
```
# 获取最新版本
latest=$(curl -sL https://api.github.com/repos/shimohq/ClickVisual/releases/latest | grep  ".tag_name" | sed -E 's/.*"([^"]+)".*/\1/')

# Mac arm64系统
wget "https://github.com/shimohq/ClickVisual/releases/download/${latest}/ClickVisual-${latest}-mac-arm64.tar.gz" -O ClickVisual-${latest}.tar.gz
```

## Linux ARM64 架构
```
# 获取最新版本
latest=$(curl -sL https://api.github.com/repos/shimohq/ClickVisual/releases/latest | grep  ".tag_name" | sed -E 's/.*"([^"]+)".*/\1/')

# Linux arm64系统
wget "https://github.com/shimohq/ClickVisual/releases/download/${latest}/ClickVisual-${latest}-linux-arm64.tar.gz" -O ClickVisual-${latest}.tar.gz
```

## 启动 ClickVisual
```
# 解压压缩包
mkdir -p ./ClickVisual-${latest} && tar -zxvf ClickVisual-${latest}.tar.gz -C ./ClickVisual-${latest}

# 修改配置文件 config/default.toml，将 MySQL、Redis 等配置改成你自己的配置。
# 修改完配置文件后，使用如下指令运行 ClickVisual
cd ./ClickVisual-${latest} && ./ClickVisual -config config/default.toml

# 访问 http://localhost:19001
# login username: shimo
# login password: shimo
```