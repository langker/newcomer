# 数据绑定

通过阅读 [Polymer Data binding](https://www.polymer-project.org/docs/polymer/databinding.html) 及其相关部分
学习 Polymer 的绑定机制.

## 问题

 - Polymer 中 `[[]]` 和 `{{}}` 的绑定有什么不同?
 - 数据绑定可以通过 `{{ foo | bar(20) }}` 传参数, 消息/事件绑定是否也有类似的方式方法?
 - Polymer 中的 publish 变量的作用是什么? publish 变量中定义 reflect 的作用又是什么?
 - 在一份自定义 Polymer 元素代码中, `this.$.foobar` 会取到哪个元素?
 - 如何监控自定义元素的变量的改变? 有几种监控的方法?

## 进阶问题

 - 模板引用(template ref)是什么? 能否单纯使用模板引用技术实现一个树形控件?
 - 如何发起一个自定义消息? 你又会如何在元素中响应这个自定义消息?
 - 如果不通过 `{{}}` 的方式进行绑定, 而是通过 Javascript 动态绑定,该如何实现?
 - 假设我有 `foo = { x: 20, y: 30 }`, 我将 foo 绑定到 Bar 元素中`<Bar value={{foo}}>`.
 此时如果我改动 foo.x 或者 foo.y 的值, Bar 元素的 fooChanged 是否会触发?
 - 倘若我绑定的 property 是一份 get/set 属性时,对这份 property 的改动如何能够触发 Polymer 的 changed 函数?

## 扩展阅读

 - [Data-binding Revolutions with Object.observe()](http://www.html5rocks.com/en/tutorials/es7/observe/) 这篇文章帮助你理解 Polymer 数据绑定背后的API和底层实现.
