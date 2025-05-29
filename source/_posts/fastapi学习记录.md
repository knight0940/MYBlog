---
title: fastapi学习记录
date: 2025-05-29 13:43:42
tags: web
categories: web前端
---

## Fastapi简介：

Fastapi是一个当下十分热门的web框架，它的特点就是简单易学,同时还有着很优秀的性能，它使用 Python 并基于标准的 Python 类型提示。由于Python是机器学习中被广泛使用的语言，这使得Fastapi与大模型的部署十分匹配。以下是Fastapi的GitHub界面，想了解更多关于Fastapi的基本概念可以自行查看https://fastapi.tiangolo.com/zh/

![1](https://fastapi.tiangolo.com/img/logo-margin/logo-teal.png)

## Fastapi中几个重要特性：

### Pydantic和Starlette:

Fastapi基于Pydantic与Starlette，所以它也继承了这两者的优秀特性。

首先是Starlette，它是Python最快的HTTP web框架之一，它有以下几点优势：

- **支持 WebSocket** 。
- **支持 GraphQL** 。
- 后台任务处理。
- Startup 和 shutdown 事件。
- 测试客户端基于 HTTPX。
- **CORS**, GZip, 静态文件, 流响应。
- 支持 **Session 和 Cookie** 。
- 100% 测试覆盖率。
- 代码库 100% 类型注释。

而Fastapi完美继承了这些优势，可以说fastapi就是Starlette的子类。

然后是Pydantic，这是一个在Python中被广泛使用的数据校验库，它主要提供了Fastapi中数据校验部分的支持，使用Pydantic可以完全不需要额外学习语法，只要了解Python type的语法就足够了，同时它对原生python支持的数据校验还做了补充，它支持对多种复杂数据如list，dict，tuple，set等数据类型的校验。值得一提的是，它还适配市面上大多数IDE，可以提供代码的自动补全支持。

这里附上它们的链接：

Pydantic：https://docs.pydantic.dev/latest/

Starlette：https://www.starlette.io/

## 可交互式文档：

说会Fastapi本身，它提供了可交互的自动生成文档，以下是来自官网的截图。可以看到下图有许多可交互界面用于测试你的api。

![](https://fastapi.tiangolo.com/img/index/index-03-swagger-02.png)

## 最重要的特性——依赖注入：

这一部分我会再后面的记录中专门详细的介绍，这里只说说它的概况。注入依赖是指将某个功能，或者模块的依赖项动态注入到路由函数或者是其他函数当中，就好比我们浏览器上的插件，它避免了重复逻辑，提高了代码的清晰度和逻辑性。
