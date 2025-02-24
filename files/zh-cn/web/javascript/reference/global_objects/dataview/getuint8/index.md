---
title: DataView.prototype.getUint8()
slug: Web/JavaScript/Reference/Global_Objects/DataView/getUint8
---
{{JSRef}}

**`getUint8()`**` 方法``从 `{{jsxref("DataView")}}相对于起始位置偏移 n 个字节处开始，获取一个无符号的 8-bit 整数 (一个字节).

{{EmbedInteractiveExample("pages/js/dataview-getuint8.html")}}

## 语法

```plain
dataview.getUint8(byteOffset)
```

## 参数

- byteOffset
  - : 偏移量，单位为字节，从头开始计算。

### 抛出错误

- {{jsxref("RangeError")}}
  - : 如果 byteOffset 超出了视图能储存的值，就会抛出错误。

## 描述

没有对齐约束; 多字节值可以从任何偏移量获取。

## 例子

```js
var buffer = new ArrayBuffer(8);
var dataview = new DataView(buffer);
dataview.getUint8(1); // 0
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 相关内容

- {{jsxref("DataView")}}
- {{jsxref("ArrayBuffer")}}
