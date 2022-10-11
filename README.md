> # default & inherit

default: 全局自定义作业的一些默认值

inherit: 选择哪些值从全局默认值中继承;


> # default 全局默认值

default 关键字下可定义如下 Key:

```shell
after_script
artifacts
before_script
cache             # 作业缓存
image             # 作业基础镜像
interruptible     # 新作业创建时，旧作业是否中断
retry
services          # 作业容器启动的服务
tags
timeout           # 作业超时时间, 默认 1 H
```

> # inherit 继承控制

inherit 可以继承 default 和 variables 这两个全局关键字，如不继承任何全局配置，可配置为 false

```yaml
job1:
  inherit:
    default: false
    variables: false
```

> 参考文档

[include](https://gitlab.gz.cvte.cn/help/ci/yaml/index.md#include)