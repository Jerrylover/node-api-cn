<!-- YAML
added: v0.7.7
changes:
  - version: v12.7.0
    pr-url: https://github.com/nodejs/node/pull/28721
    description: The stream's write() callback and return value are exposed.
-->

* `x` {number}
* `y` {number}
* `callback` {Function} 操作完成后调用。
* 返回: {boolean} 如果流希望调用的代码在继续写入附加的数据之前等待 `'drain'` 事件触发，则为 `false`，否则为 `true`。

`writeStream.cursorTo()` 将 `WriteStream` 的光标移动到指定的位置。

