---
title: "JS原型"
sidebarDepth: 2
---

# JS 原型

## 内存图

|        |            | JS 引擎  |          |        |          |     |
| ------ | ---------- | -------- | -------- | ------ | -------- | --- |
|        | 存储变量名 | Stack    | Heap     | 调用栈 | 任务队列 | ... |
| 代码区 | a          | 栈       | 堆       |        |          |     |
| 代码区 | b          | 存放数据 | 存放数据 |        |          |     |
| 代码区 | c          |          |          |        |          |     |
|        |            | 连续存储 | 链接存储 |        |          |     |

- Stack 区特点：每个数据顺序存放，存放非对象
- Heap 区特点：每个数据随机存放，存放对象

* 浏览器提供了 window，并把 console，document，对象，数组，函数都挂到了 window 上
* 挂在 window 上的东西可以在任何地方直接用（jQuery）

## 原型

- prototype 和 `__proto__` 都保存着原型的地位
- prototype 挂载函数上（构造函数）
- `__proto__`挂载每个新生成的对象上（实例）
