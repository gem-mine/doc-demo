# Gem-Mine-Doc

## 概述

这是一个基于 [docsify](https://docsify.js.org/#/) 的文档编辑系统

特性
- 无需构建，写完文档直接发布
- 基于Markdown语法
- 容易使用并且轻量 (~19kB gzipped)
- 智能的全文搜索
- 提供多套主题
- 丰富的 API
- 支持 Emoji
- 兼容 IE10+
- 支持 SSR

在它的基础上，支持了`React`代码的实时预览和编辑功能。

## 安装

本文档系统依赖 `@gem-mine/cli` 生成，请先安装 `@gem-mine/cli`

```shell
npm i @gem-mine/cli -g // 安装 gmc
gms add:doc --dir=docs// 为项目生成文档, 默认生成在当前项目的`docs`目录下
```

## 调试

```shell
gmc doc:serve
```

* `--open` option:
  * Shorthand: `-o`
  * Type: boolean
  * Default: `false`
  * Description: Open the docs in the default browser, defaults to `false`. To explicitly set this option to `false` use `--no-open`.
* `--port` option:
  * Shorthand: `-p`
  * Type: number
  * Default: `3000`
  * Description: Choose a listen port, defaults to `3000`.

## 默认插件列表

默认包含如下插件

- `search` 全文搜索
- `docsify-copy-code` 代码复制快捷键
- `emoji` emoji支持, emoji加载自`https://github.githubassets.com`
- `docsify-pagination` 翻页支持
- `docsify-tabs` 支持`tab`语法
- `prism` 语法高亮默认提供了`bash`, `json`, `javascript`, `bash`, `jsx`
- `docsify-react-live` 实现`React`代码在线查看和编辑

> 如果要扩展其他语法高亮，添加的 `prism` 请使用v15版本

!> 请务必移除`index.html`中的``<script src="../static/demo-ui-lib.js"></script>``。这是一个用作范例的组件库，请替换成你自己的组件库

## 定制

你可以尽情的修改文档目录下的内容。

请参考[官方文档](https://docsify.js.org/#/zh-cn/)