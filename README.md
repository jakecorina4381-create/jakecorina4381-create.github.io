# 个人博客

这是我的个人博客项目，基于 **Hexo** 搭建，使用 **Ayer** 主题，并部署在 GitHub Pages 上。

## 项目简介

本博客主要用于记录学习笔记、技术实践、生活随笔与个人思考。

## 技术栈

- Hexo
- Ayer Theme
- Node.js
- GitHub Pages

## 本地运行

安装依赖：

```bash
npm install
```

启动本地预览：

```bash
hexo clean
hexo g
hexo s
```

默认访问地址：

```text
http://localhost:4000
```

## 常用命令

新建文章：

```bash
hexo new "文章标题"
```

生成静态文件：

```bash
hexo g
```

启动本地服务：

```bash
hexo s
```

清理缓存：

```bash
hexo clean
```

## 项目结构

```text
.
├── .github          # GitHub Actions 配置
├── scaffolds        # 文章模板
├── source           # 博客文章、页面和静态资源
├── themes           # 主题文件
├── _config.yml      # Hexo 主配置文件
├── package.json     # 项目依赖配置
└── README.md        # 项目说明文件
```

## 部署说明

本项目使用 GitHub Pages 进行部署。

如果配置了 GitHub Actions，推送到 `main` 分支后会自动构建并部署博客。

## 博客地址

https://jakecorina4381-create.github.io

## 说明

这是一个持续完善中的个人博客项目。
