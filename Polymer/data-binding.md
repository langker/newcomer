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

### 问题4:

有以下代码:

```html
<polymer-element name="foo-bar" >
    <template>
        {{value.name}} = {{value.data.x}}, {{value.data.y}}
    </template>

    <script>
        Polymer({
            publish: {
                value: { data: {x: 0, y: 0}, name: 'no name' }
            },

            valueChanged: function () {
                console.log("value changed");
            },
        });
    </script>
</polymer-element>

<body>
    <template id="my-template" is="auto-binding">
        <foo-bar value={{foo}}></foo-bar>
        <button on-click="{{clickAction}}">change</button>
    </template>

    <script>
    var tmpl = document.querySelector('#my-template');
    tmpl.foo = { data: { x: 20, y: 30 }, name: "foobar" }
    tmpl.clickAction = function ( event ) {
        tmpl.foo.data.x = 50;
    }
    </script>

</body>
```

当按下 change 按钮的时候, 为什么页面上的元素改变了,而 valueChanged 没有被触发呢? 我要如何才能触发 valueChanged?

### 问题5:

有以下代码:

```html
<polymer-element name="foo-bar" >
    <template>
        foobar = {{value.data.x}}, {{value.data.y}}
    </template>

    <script>
        Polymer({
            publish: {
                value: { data: { x: 0, y: 0 } }
            },

            observe: {
                'value': 'valueChanged',
            },

            valueChanged: function () {
                console.log("value changed");
            },
        });
    </script>
</polymer-element>

<body>
    <template id="my-template" is="auto-binding">
        <foo-bar value={{foo}}></foo-bar>
        <button on-click="{{clickAction}}">change</button>
    </template>

    <script>
    var tmpl = document.querySelector('#my-template');
    tmpl.foo = { x_: 10, y_: 20 };
    Object.defineProperty(tmpl.foo, 'data', {
        get: function () {
            return { x: this.x_, y: this.y_ };
        },
        set: function (value) {
            this.x_ = value.x;
            this.y_ = value.y;
        }
    });

    tmpl.clickAction = function ( event ) {
        tmpl.foo.data = { x: 50, y: 100 };
    }
    </script>

</body>
```
当按下 change 按钮的时候, 为什么 valueChanged 没有被触发呢? 我要如何才能触发 valueChanged? 

## 扩展阅读

 - [Data-binding Revolutions with Object.observe()](http://www.html5rocks.com/en/tutorials/es7/observe/) 这篇文章帮助你理解 Polymer 数据绑定背后的API和底层实现.
