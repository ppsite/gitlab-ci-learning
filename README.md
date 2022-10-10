> # 模版继承与扩展

# 1. YAML 锚点继承

可以使用 YAML 锚点功能实现代码复用

```yaml
Shared: &shared
  stage: shared
  script:
    - echo "Shared scripts"

Job1:
  stage: S1
  <<: *shared
```

## Tips:

1. yaml 后添加的数据会覆盖前面的数据


# 2. extends 扩展

```shell
BaseJob1:
  stage: S1
  script:
    - echo "Base Job1 scripts"

Job1:
  stage: S1
  <<: *shared

Job2:
  extends:
    - BaseJob1
    - BaseJob2
```

## Tips:

1. 后扩展的数据会覆盖前面的数据

# 3. include

include 支持从本地，从其他项目，甚至从互联网项目中导入扩展模版，再结合 extends 实现代码复用。





> 参考文档

[include](https://gitlab.gz.cvte.cn/help/ci/yaml/index.md#include)