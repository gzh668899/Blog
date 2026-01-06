---
title: 使用 Hexo + Vercel 搭建个人博客
date: 2026-01-06 22:31:43
tags: [Hexo, Vercel, 博客]
categories: 技术记录
---

## 前言

一直想搭建一个属于自己的个人博客，用来记录生活和学习。经过一番调研，最终选择了 **Hexo + Vercel** 的方案。

## 为什么选择这个方案

### 技术选型对比

| 框架 | 语言 | 构建速度 | 特点 |
|------|------|---------|------|
| Hexo | Node.js | 中等 | 中文生态好，主题丰富 |
| Hugo | Go | 最快 | 性能极佳，配置简单 |
| VitePress | Vue/Node.js | 快 | 现代化，适合技术文档 |
| Astro | Node.js | 快 | 架构灵活，零默认JS |

最终选择 **Hexo**，因为：
- 中文社区成熟，遇到问题容易解决
- 主题丰富，Fluid 主题颜值很高
- 文档齐全，上手容易

### 部署平台选择

- **Vercel**：速度快，自动 HTTPS，支持自定义域名，国内访问体验好
- **Cloudflare Pages**：全球 CDN，也是很好的选择
- **GitHub Pages**：简单稳定，但国内访问较慢

最终选择 **Vercel**，主要是看重它的部署速度和稳定性。

## 搭建步骤

### 1. 安装 Hexo

```bash
npm install -g hexo-cli
hexo init my-blog
cd my-blog
npm install
```

### 2. 配置博客

编辑 `_config.yml` 文件，设置博客的基本信息：

```yaml
title: 我的博客
subtitle: 记录生活与思考
description: 轻量级个人博客
author: 你的名字
language: zh-CN
timezone: Asia/Shanghai
```

### 3. 安装主题

我选择的是 **Fluid** 主题，设计现代、功能完善：

```bash
npm install hexo-theme-fluid --save
```

修改 `_config.yml`：

```yaml
theme: fluid
```

### 4. 本地预览

```bash
hexo generate
hexo server
```

访问 `http://localhost:4000` 即可预览。

### 5. 部署到 Vercel

1. 将代码推送到 GitHub
2. 在 Vercel 导入仓库
3. 点击 Deploy，等待部署完成

就这么简单！

## 写新文章

```bash
hexo new "文章标题"
```

文章会生成在 `source/_posts/` 目录，使用 Markdown 格式编写。

## 总结

整个搭建过程非常顺畅，Hexo + Vercel 是一个非常轻量且高效的博客方案。如果你也想搭建自己的博客，强烈推荐尝试！

## 参考链接

- [Hexo 官方文档](https://hexo.io/zh-cn/docs/)
- [Fluid 主题文档](https://hexo.fluid-dev.com/docs/)
- [Vercel 官网](https://vercel.com/)
