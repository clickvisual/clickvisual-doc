# 变更日志

## ClickVisual 版本 2022-11-25 v0.4.4

[https://github.com/clickvisual/clickvisual/releases/tag/v0.4.4](https://github.com/clickvisual/clickvisual/releases/tag/v0.4.4)

### 功能
- 支持检索条件收藏
- 支持企业微信告警推送
- 支持按标签输入查询语句
- 定时任务失败后推送该告警
- 日志查询框兼容粘贴多行代码
- 拓扑图增加副本和分片数量显示
- 告警规则下发支持 Prometheus Operator
- 告警数据存储表 metrics.samples 一键创建
- 支持通过模板方式创建 EGO 框架支持的全套日志库

### 优化&修复

- 告警推送模块代码重构
- 趋势图数据计算逻辑优化
- 查询语句自动填充逻辑调整
- 更新 swagger 文档展示样式
- 链路日志库支持单页数据条数配置
- 支持聚合告警模式下日志详情读取推送
- 修复时间轴分辨率错误和表模式数据显示异常
- 修复使用分布式表产生的告警数据的问题

### 新贡献者
* @pigcsy made their first contribution in [https://github.com/clickvisual/clickvisual/pull/725](https://github.com/clickvisual/clickvisual/pull/725)

## ClickVisual 版本 2022-10-28 v0.4.3

[https://github.com/clickvisual/clickvisual/releases/tag/v0.4.3](https://github.com/clickvisual/clickvisual/releases/tag/v0.4.3)

### 功能
- 告警模块
  - 独立告警配置，增加基础组件环境检测包括 prometheus/alertmanager，并进行 remote_read 配置检测
  - 告警规则下发时增加【配置中】状态，在完成 prometheus 规则加载检测后，变更为【正常】
  - 支持多条件告警
- 拓扑页面支持节点建表语句查询
- 支持按照 select 字段次序显示结果
- 日志查询提示，记录查询历史以及常用函数提示

### 优化&修复
- 支持数组显示以及点击查询
- 链路库展示兼容更多的日期格式
- 日志查询编辑器更改为 codemirror
- 修复隐藏字段权限检测错误
- 修复日志库潜在的事务锁定问题
- 修复日志库链路模式下的错误显示，兼容大小写样式
- 修复集群中已有日志库添加告警规则提示的 cluster 缺失问题


## ClickVisual 版本 2022-09-30 v0.4.2

[https://github.com/clickvisual/clickvisual/releases/tag/v0.4.2](https://github.com/clickvisual/clickvisual/releases/tag/v0.4.2)

### 功能
- 增加对链路日志库数据分析功能
- 用户管理模块，基础 CURD 和用户密码重置功能

### 优化&修复
- clickhouse-go 升级为 v2.3.0，并支持 http 和 https 协议 [@laojianzi](https://github.com/laojianzi)
- 优化已接入日志时间字段筛选逻辑，使用 like 方式进行过滤 [@shushenghong](https://github.com/shushenghong)
- 链路日志库增加更多数据展示
- 一般日志库与链路日志库跳转交互优化
- 从分析日志内容格式来确认日志库类型，调整为通过具体的用户配置来进行确认
- 告警列表支持 id 过滤，避免同名产生的误导
- 删除对集群中非必要数据进行的 watch 逻辑
- 针对大量数据的缓慢日志渲染进行了优化
- 链路日志库分析落地数据库创建失败问题
- 对不同时间区间使用不同的时间精度来显示时间点
