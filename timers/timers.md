
<!--introduced_in=v0.10.0-->

> 稳定性: 2 - 稳定

`timer` 模块暴露了一个全局的 API，用于预定在将来某个时间段调用的函数。 
因为定时器函数是全局变量，所以不需要调用 `require('timers')` 来使用 API。

Node.js 中的定时器函数实现了与 Web 浏览器提供的定时器 API 类似的 API，但是使用了不同的内部实现（基于 Node.js [事件循环][Event Loop]构建）。


