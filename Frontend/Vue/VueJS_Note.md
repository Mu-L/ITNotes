---
aliases: []
tags:
  - front-end
  - vue
  - vuejs
created: 2023-08-18 19:44:52
modified: 2026-07-08 20:16:10
---

# VueJS 笔记

---

## 目录

* [Vue CLI](#Vue%20CLI)

---

## 简介

[Vue.js](https://vuejs.org) 是一个用于构建用户界面的渐进式框架。

> [!info] 
> 
> 渐进式意味着你可以根据项目需要，只引入 Vue 的一部分能力：从一个简单的页面交互增强，到构建完整的单页应用（SPA），乃至服务端渲染（SSR）应用，Vue 都能胜任。

Vue3 ，于 2020 年 9 月 18 日正式发布。

相比 Vue2，Vue3 对核心架构进行了全面重写：

* 响应式系统从 `Object.defineProperty` 升级为 `Proxy`
* 引入「**组合式 API**」（Composition API），并在性能、[TypeScript](../../JS/TypeScript/TypeScript_Note.md) 支持、包体积等方面全面提升

GitHub：

* [Vue 3](https://github.com/vuejs/core)
* [Vue 2](https://github.com/vuejs/vue)

---

## Vue CLI

### 安装及升级

#### 安装

```shell
npm install -g @vue/cli
```

> [!info] 
> 
> 老版本的包名是 `vue-cli`。从 3.x 开始的版本是包的名字叫`@vue/cli`。但安装完成后，调用的命令都是`vue`。
> 
> 防止冲突，如果有之前的 2.x 版本的，最后使用 `npm install` 命令卸载掉，再装新版本。
> 
>> [!tip] 
>> 
>> 安装完成后，可以使用 `vue --version`，查看其版本。
>> 
>> ```shell
>> $ vue --version
>> @vue/cli 5.0.9
>> ```

#### 升级

```shell
npm update -g @vue/cli
```

### 创建项目

使用 `create` 命令创建项目：

```
vue create 项目名
```

> [!info] 
> 
> 项目名，即是在当前路径下，创建一个以此项目名为目录名的子目录，作为此 vue 项目的根目录。

这时会出现下拉选项：

```shell
Vue CLI v5.0.9
? Please pick a preset: (Use arrow keys)
❯ Default ([Vue 3] babel, eslint) 
  Default ([Vue 2] babel, eslint) 
  Manually select features 
```

前两个是默认，只是版本不同。

最后一个是手动，选择手动（Manually）就又会出现下拉菜单，让你勾选功能：

```shell
Vue CLI v5.0.9
? Please pick a preset: Manually select features
? Check the features needed for your project: (Press <space> to select, <a> to toggle all, <i> to invert selection, and <enter> 
to proceed)
 ◉ Babel
 ◉ TypeScript
 ◉ Progressive Web App (PWA) Support
 ◉ Router
 ◉ Vuex
 ◉ CSS Pre-processors
 ◉ Linter / Formatter
❯◉ Unit Testing
 ◯ E2E Testing


```

> [!info] 
> 
> 就出现功能选项，可根据需要自行勾选（使用空格勾选，使用 `i` 取消选中）,选择完成后，回车确认。

---

## 相关笔记

* [Vue 视频清单](VueJS_Videos.md)
* [前端笔记](Front-end_Note.md)
* [NodeJS 笔记](../../Node/NodeJS_Note.md)

