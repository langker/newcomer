# DOM 消息模型

Web 编程的基础之一是理解 DOM 消息模型,而 DOM 消息模型其实就只有两种,Capture Phase 和 Bubble Phase.

## 阅读

通过阅读 [Event Order](http://www.quirksmode.org/js/events_order.html), [Bubbling and capturing](http://javascript.info/tutorial/bubbling-and-capturing), [Javascript Events – Capturing And Bubbling](http://themousepotatowebsite.co.za/javascript-events-capturing-and-bubbling/) 对 DOM 的消息传递有
个初步的了解.之后可以通过这个 [Demo](http://themousepotatowebsite.co.za/demo/2011-11-03-javascript-events-capturing-and-bubbling/) 更进一步认识.

## 深入阅读

[DOM-Level-3-Events](http://www.w3.org/TR/DOM-Level-3-Events/) 是讲解 DOM 消息模型的标准文档,可以通过
对他的阅读深入理解 DOM 消息模型.

[http://stackoverflow.com/questions/2661199/event-capturing-vs-event-bubbling](http://stackoverflow.com/questions/2661199/event-capturing-vs-event-bubbling) 这里讨论了 capture phase 和 bubble phase 他们各自应用的地方.

## 问题

 - 如何停止消息的传递?
 - preventDefault() 和 stopPropagation() 的区别是什么?
 - 除了浏览器本身的派发的消息外,你该如何通过 Javascript 派发消息?
 - 有 A, B, C 三个元素, A 嵌套 B 嵌套 C ( A>B>C ), 他们大小相等, 当鼠标从 C 元素外移动进入 C 元素内时, 都发送了哪些消息?
 - 你觉得什么时候应该监听 Capture Phase 的消息, 什么时候应该监听 Bubble Phase 的消息?
