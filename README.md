> # Job & Stage

---
默认 stage

```yaml
stages:
  - .pre
  - build
  - test
  - deploy
  - .post
```

Job 可以属于 Stage，但并非所有的 Job 都必须要属于某个 Stage