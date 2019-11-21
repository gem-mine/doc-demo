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

### 安装

本文档系统依赖 `@gem-mine/cli` 生成，请先安装 `@gem-mine/cli`

```shell
npm i @gem-mine/cli -g // 安装 gmc
gms add:doc // 为项目生成文档, 默认生成在当前项目的`docs`目录下
```

### 调试

```shell
npm run dev:doc // 执行的`gmc doc:serve`
npx gmc dev:doc --no-open
```

``dev:doc`` 支持如下参数

* `--port`:
  * 默认值: `3000`
  * 描述: 开启的调试服务器的调试端口，会自动检测冲突并递增寻找可用端口
* `--livereloadPort`:
  * 默认值: `35729`
  * 描述: 用于实时刷新的端口，会自动检测冲突并递增寻找可用端口
* `--indexName`:
  * 默认值: `index.html`
  * 描述: 开启后默认打开的HTML入口页面
* `--open`:
  * 默认值: true
  * 描述: 开启调试服务器后自动打开浏览器，传入`--no-open`来关闭开打浏览器

## 默认插件列表

默认包含如下插件

- `search` 全文搜索
- `docsify-copy-code` 代码复制快捷键
- `emoji` emoji支持, emoji加载自`https://github.githubassets.com`
- `docsify-pagination` 翻页支持
- `docsify-tabs` 支持`tab`语法
- `prism` 语法高亮默认提供了`bash`, `json`, `javascript`, `bash`, `jsx`
- `docsify-plugin-toc`实现了右侧目录
- `docsify-example-panels` 实现了左右分布的块元素
- `docsify-react-live` 实现`React`代码在线查看和编辑

> 如果要扩展其他语法高亮，添加的 `prism` 请使用v15版本

!> 请务必移除`index.html`中的``<script src="../static/demo-ui-lib.js"></script>``。这是一个用作范例的组件库，请替换成你自己的组件库

## 定制

你可以尽情的修改文档目录下的内容。

请参考[官方文档](https://docsify.js.org/#/zh-cn/)