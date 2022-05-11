# Auth Proxy

你可以将 clickvisual 配置为让 HTTP 反向代理处理身份验证，通过这种方式你可以很方便的将 clickvisual 嵌入到其他系统里。下面我们详细介绍 auth proxy 的配置选项。



HTTP Proxy 配置：
```yaml
[auth.proxy]
# Defaults to false, but set to true to enable this feature
enabled = true
# HTTP Header name that will contain the username or email
headerName = "X-WEBAUTH-USER"
```

使用 Curl 测试 clickvisual 的 AuthProxy 功能：
```sh
curl -H "X-WEBAUTH-USER: admin"  http://localhost:19001/api/v1/users/info
```

第三方系统通过 AuthProxy 嵌入clickvisual：

![img.png](../../images/auth-proxy.png)image.png