# 使用说明

日志查询条件筛选部分使用的 ClickHouse 原生 Where 子句语法。

[官方文档](https://clickhouse.com/docs/zh/sql-reference/statements/select/where)

## 阿里云语法对照

### 精确查询
阿里云
```
lv: debug
```

ClickVisual
```
lv='debug'
```

### 模糊匹配

阿里云
```
debug
```

ClickVisual
```
_raw_log_ like '%debug%'
```

