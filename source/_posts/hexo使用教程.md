---
title: hexo使用教程
date: 2023-04-28 10:53:24
category: hexo教程
---

# 开始

## 进入 d:\blog 文件夹

hexo 必须在这个目录下才可运行

## 启动 hexo

`hexo serve`

## 创建新的博客

通过 `hexo new "My New Post"` 生成.md 文档，修改 tags 为 category 进行分类

## 将文件部署到 github 公共域名上

`hexo clean` 进行清理缓存等.
`hexo generate` 生成 html 文件.
再通过 `hexo deploy` 进行部署到远程仓库.

## 修改名字

在 d:\blog 下找到\_config.yml，修改 author 名字，即可换作者名称.

# 备份教程

在 blog 目录下新建仓库，并关联远程.
`git remote set-url origin git@github.com:zyyy9/zyyy9.github.io.git`
`git add .`
`git commit -m "提交信息"`
`git push origin blog`

# markdown 语法

<https://markdown.com.cn/>

# hexo 官方文档

<https://hexo.io/zh-cn/docs/index.html>
