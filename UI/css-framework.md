# 前端UI框架基础

前端UI框架是 Html、CSS 和 JS 的功能集合，将 web 开发交互界面里常用的页面布局、控件结构和排版方式以预定义的 Class 形式组合成 UI 库。Web 开发人员可以通过`<div class="myClass">`的方式快速实现页面的布局和表现。

## 主流前端框架

- Bootstrap <http://www.bootcss.com/>
- Foundation <http://foundation.zurb.com/>
- SemanticUI <http://semantic-ui.com/>

关于他们的特性和对比，可以参考这篇文章：[Bootstrap vs Foundation vs Semantic-UI 前端框架评估](https://tower.im/projects/5ddd2d4f1bc24ef58b6fb66a53190150/messages/51d8cb2a802849bfa702e5ea99af3c30/)

目前火盒团队的内网和官方网站使用的是 Foundation 框架，学习 Foundation 时可以参考之前写的[学习笔记](https://tower.im/projects/75be4d4c1eba48278e512b2b97e476ea/todos/1782787419f04a0ea8cd03acaa9c92fb/)。

## 样式表扩展语言

为了对框架中的样式表做更深入的功能开发，通常CSS前端框架会使用一种样式表扩展语言，这类语言为 CSS 加入了脚本语言的基础功能，比如定义变量、逻辑判断、使用函数和继承等等。

不同的框架选择不同的样式表扩展语言：

- Bootstrap：[Less](http://www.bootcss.com/p/lesscss/)
- Foundation: [Sass](http://www.w3cplus.com/sassguide/syntax.html)
- Docpad 和 Fireball-x：[Stylus](http://www.zhangxinxu.com/jq/stylus/selectors.php)

如果有能力也可以阅读官方英文文档：
- Less: <http://lesscss.org/>
- Sass: <http://sass-lang.com/>
- Stylus: <http://learnboost.github.io/stylus/>

总的说来这些扩展语言大同小异，可以互相参考着一起掌握基础。

## 学习任务

- 参考文档，尝试在本地安装和建立不同 UI 框架的项目
- 参考 UI 框架的控件库，对新建项目里的初始页面进行个性化定制
- 安装配置火盒手册和火盒官网的 docpad 项目，并参考 [docpad](https://docpad.org/) 文档和 foundation 文档了解网站的架构。


> Written with [StackEdit](https://stackedit.io/).
