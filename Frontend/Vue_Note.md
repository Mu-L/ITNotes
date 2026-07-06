---
aliases: []
tags: []
created: 2023-08-18 19:44:52
modified: 2026-07-07 02:26:38
---

# Vue 笔记

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

---

## 相关笔记

* [Vue 视频清单](Vue_Videos.md)
* [前端笔记](Front-end_Note.md)
* [NodeJS 笔记](../Node/NodeJS_Note.md)

