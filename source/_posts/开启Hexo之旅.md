---
title: 开启Hexo之旅
keywords: 教程
cover:
  - https://www.logosc.cn/uploads/resources/2018/11/29/1543459457_thumb.jpg
sticky: 1
banner:
  type: img
  bgurl: https://pic1.zhimg.com/v2-b3c2c6745b9421a13a3c4706b19223b3_r.jpg
  bannerText: Hi my new friend!
toc: false
date: 2024-03-05 18:10:56
categories: 
- hexo教程
tags:
- 教程
- 必读博客
---

本文将阐述如何在cmd创建页面及博客的简单应用方法
## 快速开始

#### 新建博客
``` bash
hexo new [博客名]
```
###### 博客头部信息：
``` yml
keywords：关键字，用于 meta 标签
description：描述，用于 meta 标签
cover：文章封面图，可为字符串或数组，如果数组长度为 2 则会根据主题自动切换。
sticky：首页排序值
banner：文章页横幅背景，字段参考 横幅 banner.default 字段。
toc：是否显示目录，仅当值为 false 生效。默认通过 _config.async.yaml 的 toc 控制。
single_column：单栏显示详情页，为 true 时生效。
author：文章作者
originalLink：文章源链接（用于转载）
```

#### 新建草稿
``` bash
hexo new draft [博客名]
```
此时博客页面不显示此文
###### 发布草稿
``` bash
hexo publish [博客名]
```

#### 归档
个人理解为可以查看所有文章

#### 访问about、categories页面
要访问about和categroies页面，暂时只能通过手动输入url来访问。
``` http
http://地址:端口/about
http://地址:端口/categories
```

#### 分类
在最上方头部信息中添加categories
``` yml
categories:
- 分类名
```
注意：一个md只能添加一个分类。如果有多个分类，例如
``` yml
categories:
- 类1
- 类2
```
则表示该博客属于类1中的类2分类

#### 标签
在最上方头部信息中tags添加信息
``` yml
tags:
- tag1
- tag2
```
一篇文章可以拥有多个tag

#### about
新建关于页面
``` bash
hexo new page about
```
进入 source/about/index.md，设置 layout 字段
``` yml
title: 关于
layout: about
```
如果使用内置模板，可以设置 _config.yml 中的 about
``` yml
about:
  insert: none # 插入规则 before（插入在内容前） | after（插入在内容后） | none（不插入）
  title: # 标题
  introduction: # 个人简单描述
  blog: # 博客信息
  privacy: # 隐私权说明
```

#### 参考文档
> [hexo-theme-async官方文档](https://hexo-theme-async.imalun.com/guide/)
> [hexo官方文档](https://hexo.io/zh-cn/docs/)