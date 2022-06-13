# 已有数据表接入

`可用版本 >= 0.2.2`

在系统设置中新增实例。

![img.png](../../images/instance-manager.png)

点击新增日志库，选择`已有日志库`，时间解析字段是日志数据时间轴字段，可选类型为`DateTime64(3)`、`DateTime`、`Int32`、`Int64`，目标数据表需要包含其中一种类型的字段，才可以正常接入。

![img.png](../../images/exist-table-choice.png)
