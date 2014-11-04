# 制作一个简单的 GameObject Pool

## 任务

我们知道在 Unity3D 中使用 Object.Destroy() 和 Object.Instantiate() 或者 new GameObject()
都有cpu开销,并且 new 或 instantiate 会引起 Mono C# 的 heap 分配，从而增加垃圾回收的压力.

在游戏中,我们会通过预先分配的 GameObject Pool 来避免频繁添加和删除的 GameObject 的 new 和
destroy 行为.

请实现这样一个 Pool 数据结构,可以在游戏开始前,进行初始化.在游戏进行中,用户可以向 pool 申请和归还
GameObject.

不用考虑pool的动态增长,当 pool 内的 GameObject 不够申请时,直接报错即可.
