> # 模版继承与扩展

# YAML 锚点继承

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

> 实验证明

# extends 扩展

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