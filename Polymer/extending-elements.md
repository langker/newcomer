# 扩展已有元素

Polymer 的元素是可以继承并扩展的, 在 [Polymer API developer guide](https://www.polymer-project.org/docs/polymer/polymer.html)
 中的 Extending other elements 一节中你可以学习到如何扩展元素.

值得一提的是,Polymer 中有一些文档里没有特别说明的特殊元素,但是在实际开发应用中却常常被用到.

## <content> 元素

这个元素可以让你的自定义 Element 下的直系 children 进入到 shadow DOM 中你标记的内容标签 <content> 里.
但是进入到内容标签中的 Element 并不享受 shadow DOM 的样式规则.

举个例子,假设我们这么定义标签:

```html
<polymer-element name="foo-bar" >
    <template>
        <style>
            .foo {
                font-size: 12px;
                color: blue;
            }
        </style>

        Foobar list:
        <content></content>
    </template>
    <script>
        Polymer({
        });
    </script>
</polymer-element>
```

在代码中有如下应用:

```html
<style>
    .foo {
        font-size: 12px;
        color: red;
        margin-left: 20px;
    }
</style>

<body>
    <foo-bar>
        <div class="foo">Foobar 01</div>
        <div class="foo">Foobar 02</div>
        <div class="foo">Foobar 03</div>
        <div class="foo">Foobar 04</div>
        <div class="foo">Foobar 05</div>
        <div class="foo">Foobar 06</div>
        <div class="foo">Foobar 07</div>
        <div class="foo">Foobar 08</div>
    </foo-bar>
</body>
```

此时, content 里的字样还是沿用红色而不是 Shadow DOM 里定义的蓝色.

## <shadow> 元素

<shadow> 元素在文档 Extending other elements 里有记录, 他是用于将父类标签的 Shadow 内容在子类标签中重用
的方法.

## 问题

  - 我希望在子类中调用父类的方法,在 Polymer 中是如何来操作的?
  - 假设我扩展了一个父类标签,我希望通过重写局部的 css 来改变继承过来的父类标签中的某些样式, 我该如何操作?
