---
aliases: []
tags:
  - front-end
  - vue
  - vuejs
created: 2023-08-18 19:44:52
modified: 2026-07-07 02:45:16
---

# VueJS 笔记

---

## 目录

* [Vue CLI](#Vue%20CLI)

---

## 简介

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

