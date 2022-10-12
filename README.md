> # needs & dependencies

# 作业依赖 - needs

默认情况下，所有 Job 按照 stages 规定的顺序执行，上一个 stage 结束后，才能执行下一个 stage

但对于一些并行构建模式，无需等待上一个阶段的所有作业完成，就可以继续执行下一个构建；这样可以大大缩短构建时间。

![](./images/default-pipline.png)

`如上图所示，Test 未执行完，Deploy 不会执行`

