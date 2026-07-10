---
aliases: []
tags:
  - javascript
  - js
  - es
  - ecmascript
created: 2023-01-31 11:31:14
modified: 2026-07-09 21:26:18
---

# JavaScript 笔记

## 目录

* [使用](#使用)
* [语法](#语法)
* [工具](#工具)
	* [ESLint](#ESLint)

---

## 使用

### 标签

`<script>` 标签有一些现在很少用到的特性（attribute）,在老的 [HTML4](../Frontend/Html_Note.md#HTML4) 中是要求 `script` 标签要有 `type` 属性，通常是 `type="text/javascript"`。现代 [HTML](../Frontend/Html_Note.md#HTML5) 标准已经不需要这样的属性声明了。

#### 外部 JS

```javascript
<script src=".../...js"></script>
```

> [!tip] 
> 
> 如果设置了 `src` 特性，`script` 标签内容将会被忽略。
>
> 也就是说设置了 `src` 属性的 `script` 标签失去了普通 `script` 标签的「包裹」代码的功能，它的唯一功能就是**引入**外部 JS 文件。

---

## 语法

* [JS 语法笔记](JS_Syntax.md)

---

## 工具

### ESLint

[ESLint](https://eslint.org) 是 JavaScript 的一个 Linter 工具，即「代码检查工具」。

#### 安装

全局安装：

```shell
npm install eslint --global
```

#### 相关文档

* [Getting Started with ESLint](https://eslint.org/docs/latest/use/getting-started)
* [配置文件 - ESLint 中文文档](https://nodejs.cn/eslint/configuring/configuration-files/)

---

## <span id="jsn_aboutlinks">相关链接</span>

* [JavaScript 文档 - MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript)

---

## 相关笔记

* [JS 语法笔记](JS_Syntax.md)
* [JS 资料清单](JS_Material.md)
* [JS 视频清单](JS_Videos.md)
* [前端笔记](../Frontend/Front-end_Note.md)

