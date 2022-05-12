# 常见问题

## 服务启动后跳转到 localhost
### 现象
![img.png](../../images/qa-1.png)

### 解决
服务配置中包含地址设置，调整这个地址即可
```toml
[app]
rootURL = "http://localhost:19001"
 ```
- 此处的rootURL 必须有http:// 前缀，不然会是一个非法的url不能使用

配置文件对应地址
- docker：/data/all-in-one/clickvisual/config/docker.toml
- 代码启动：/config/default.toml