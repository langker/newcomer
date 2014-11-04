# 了解 Unity3D 中的更新方法

请阅读和学习 [Execution Order of Event Functions](http://docs.unity3d.com/Manual/ExecutionOrder.html)
并回答以下问题

## 问题

 - 在 Unity3D 中有哪些更新物体状态的函数和方法?
 - 这些方法分别在 Unity3D 游戏运行中的一帧中的什么时候对物体进行更新?
 - 应该如何合理利用不同的更新函数或方法?

## 任务

假设由你来实现 Unity3D 引擎中,游戏运行时一帧的运行逻辑,你会如何来实现这个 mainloop 函数? 请使用
你熟悉的语言来书写这个 mainloop 函数. 已知 GameObject 存放于 GameObject[] gameObjects 中.
