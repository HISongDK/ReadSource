# axios 工具函数

一些用于判断数据类型是否符合预期的函数

## 主要方式

- 使用 `typeof` 直接判断参数是否为指定的数据类型
- 使用 `Function.prototype.call` 让指定参数调用 `Object.prototype.toString`方法 ，看结果字符串是否符合预期

## 源码

## API

- [`Object.prototype.toString`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/toString)
- [`Function.prototype.call`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Function/call)
