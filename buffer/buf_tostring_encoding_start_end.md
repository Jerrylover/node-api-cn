<!-- YAML
added: v0.1.90
-->

* `encoding` {string} 使用的字符编码。**默认值:** `'utf8'`。
* `start` {integer} 开始解码的字节偏移量。**默认值:** `0`。
* `end` {integer} 结束解码的字节偏移量（不包含）。**默认值:** [`buf.length`]。
* 返回: {string}

根据 `encoding` 指定的字符编码将 `buf` 解码成字符串。
传入 `start` 和 `end` 可以只解码 `buf` 的子集。
如果输入中的字节序列在给定的 `encoding` 中无效，则将其替换为替换字符 `U+FFFD`。

字符串的最大长度（以 UTF-16 为单位）可查看 [`buffer.constants.MAX_STRING_LENGTH`]。

```js
const buf1 = Buffer.allocUnsafe(26);

for (let i = 0; i < 26; i++) {
  // 97 是 'a' 的十进制 ASCII 值。
  buf1[i] = i + 97;
}

console.log(buf1.toString('ascii'));
// 打印: abcdefghijklmnopqrstuvwxyz
console.log(buf1.toString('ascii', 0, 5));
// 打印: abcde

const buf2 = Buffer.from('tést');

console.log(buf2.toString('hex'));
// 打印: 74c3a97374
console.log(buf2.toString('utf8', 0, 3));
// 打印: té
console.log(buf2.toString(undefined, 0, 3));
// 打印: té
```

