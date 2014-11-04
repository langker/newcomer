# 元素生命周期

Polymer 的元素从创建到结束有以下几个时间点: created, ready, attached, domReady, detached.
请阅读 [Polymer API developer guide](https://www.polymer-project.org/docs/polymer/polymer.html)
中的 Element lifecycle methods 章节获取更多的信息.

## 问题

### 问题1: 元素的 ready 和 domReady 有什么区别,一般如何使用他们?

### 问题2: 以下数据段定义中,哪些地方不合理? 如何操作更合适, 为什么?

```js
Polymer({
  foo: 'foo',
  bar: 'bar',
  foobar: [],
  settings: {
    text: 'hello foobar'
  },

  created: function () {  
  },

  ready: function () {
    console.log('foobar ready!');
  },
});
```
