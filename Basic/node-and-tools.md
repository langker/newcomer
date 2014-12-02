# 了解 Node.js 以及相关工具

Node.js 在火盒团队的开发中占有非常重要的地位. 从项目编译,后台服务以及主引擎编辑器的开发都涉及到 Node.js 技术.
了解和掌握 Node.js 是团队成员的必修课之一. 本篇文章的学习主要以了解 Node.js 为主, 实际编程请通过自己课后练习,
以及实际项目运用中进行掌握.

## 安装与学习

火盒项目中使用的是 Node.js v0.11.+ 的版本，Mac/Linux 用户建议通过 http://nodejs.org/dist/ 找到 v0.11.+ 进行安装，Windows 用户由于 gulp 依赖库的一个 bug 请暂时直接从[主页](http://nodejs.org)下载当前的 v0.10 版，如果主页君更新到了 v0.11 请到 http://nodejs.org/dist/ 找到最后一个 v0.10.+ 版本进行安装。  
Node.js 的学习可以通过 Node.js 官方的文档,以及 [Node School](http://nodeschool.io/).

## 相关工具

### npm

npm 是 Node.js 的包管理工具,可以通过 https://www.npmjs.org/doc/ 快速学习和掌握.

### bower

bower 是我们用于管理页面包的工具,功能与 npm 类似,只是他负责的是页面包的管理,npm 负责的是 node.js 模块包的管理.
可以通过 http://bower.io/ 学习和使用 bower.

### gulp

gulp 是我们用于项目过程中的编译环节的开发工具. 可以通过 http://gulpjs.com/ 学习和使用.  
也可参考[Fireball core 开发入门教程](https://tower.im/projects/5ddd2d4f1bc24ef58b6fb66a53190150/messages/3ad888e2e0d34b559c25a7eca852d458/)中的步骤五。

## 练习题

 1. 请通过 Node.js 搭建一个简单的 Web 服务器 (可以使用 express).
 1. 通过 bower 下载 pixijs.
 1. 调整 [Pixi](http://www.pixijs.com/examples/) 页面中 Example 18 的源码使其可以运行在你搭建的 web 服务器中.

## 练习题2

 1. 将上面的 [Pixi Example 18](http://www.pixijs.com/examples/) 源代码部分从 html 页面抽离.
 1. 使用 gulp 对抽离的源代码进行静态分析 (gulp-jshint) 和 minified (gulp-uglify) 操作.
 1. 将编译后的 js 运行于抽离后的 html 页面.
