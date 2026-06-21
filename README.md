# LE.乐｜Obsidian × Hexo 个人知识发布系统

这是我的个人博客项目，基于 **Obsidian + Hexo + Ayer Theme + GitHub Pages** 搭建。

项目的核心目标是：把 Obsidian 中的学习笔记、AI 新闻周报、GitHub 热门项目推荐、旅行摄影内容，整理并发布为结构清晰、长期可维护的公网博客。

## 在线访问

博客地址：

https://jakecorina4381-create.github.io

## 项目简介

这个项目不仅是一个普通的 Hexo 博客，更是一套个人知识发布流程。

我使用 Obsidian 进行日常写作和资料整理，使用 Codex 辅助完成 Markdown 格式转换、图片路径修正和 Hexo 文章生成，最后通过 Hexo 生成静态网站，并部署到 GitHub Pages。

整体流程如下：

```text
Obsidian 写作
    ↓
Codex 格式转换
    ↓
Hexo 生成博客
    ↓
GitHub Pages 公网发布
```

## 主要栏目

目前博客主要包含以下内容：

* **AI 新闻周报**：整理每周值得关注的 AI 公司、模型、产品与行业动态
* **每周 GitHub 热门项目介绍**：精选近期值得关注的开源项目和开发者工具
* **学习笔记**：记录课程学习、技术实践和工具使用经验
* **旅行见闻**：整理旅行过程中的观察、记录和照片
* **摄影作品**：展示个人摄影图片与相关说明
* **生活随笔**：记录阶段性思考和生活感悟

## 功能特性

* 使用 Hexo 构建静态博客
* 使用 Ayer 主题进行页面展示
* 支持 GitHub Pages 公网访问
* 支持 Obsidian Markdown 内容转换为 Hexo 文章
* 支持文章分类、归档与图片展示
* 支持旅行、摄影、关于我等独立页面
* 保留文章标签信息，但不单独展示标签页面
* 适合长期维护个人知识库与公开博客

## 技术栈

* Hexo
* Ayer Theme
* Node.js
* GitHub Pages
* Git / GitHub
* Obsidian
* Codex

## 项目结构

```text
blog
├─ _config.yml              # Hexo 站点配置
├─ package.json             # 项目依赖配置
├─ source
│  ├─ _posts                # 博客文章目录
│  ├─ about                 # 关于我页面
│  ├─ images                # 博客图片资源
│  ├─ photos                # 摄影页面
│  └─ travel                # 旅行页面
├─ themes
│  └─ ayer                  # Hexo 主题
├─ scaffolds                # Hexo 文章模板
└─ README.md                # 项目说明文档
```

## Obsidian 到 Hexo 的发布流程

每次从 Obsidian 发布文章到 Hexo，大致流程如下。

### 1. 在 Obsidian 中写好文章

常用目录示例：

```text
Horizon / Weekly / AI-News
Horizon / Weekly / GitHub
Horizon / Assets / github
Horizon / Assets / screenshots
```

### 2. 复制 Obsidian 原文路径

在 Obsidian 中右键文章，选择：

```text
在系统资源管理器中显示
```

然后在 Windows 文件资源管理器中：

```text
Shift + 右键 .md 文件 → 复制为路径
```

### 3. 在 Hexo 中新建文章

进入 Hexo 根目录：

```powershell
cd 'D:\下载\hexo\blog'
```

新建 GitHub 热门项目文章：

```powershell
hexo new "2026.6.28 本周GitHub热门项目介绍"
```

新建 AI 新闻周报文章：

```powershell
hexo new "2026.6.28 AI新闻周报"
```

文章会生成到：

```text
source/_posts
```

### 4. 使用 Codex 转换文章格式

Codex 主要负责：

* 删除 Obsidian 原始属性区
* 添加 Hexo front-matter
* 保留正文内容
* 转换 Obsidian 双链
* 转换 Obsidian 图片语法
* 复制图片到 Hexo 图片目录
* 检查 Markdown 格式和图片路径

Obsidian 图片语法示例：

```markdown
![[Horizon/Assets/github/example.png]]
```

需要转换为 Hexo 可识别的标准 Markdown 格式：

```markdown
![项目截图](/images/github/example.png)
```

图片文件放入：

```text
source/images/github
```

或：

```text
source/images/ai-news
```

### 5. 本地预览

```powershell
hexo clean
hexo g
hexo s
```

然后访问：

```text
http://localhost:4000
```

检查文章、归档、分类、图片和排版是否正常。

### 6. 同步源码到 GitHub

```powershell
git status
git add .
git commit -m "update blog"
git pull --rebase origin main
git push origin main
```

### 7. 部署到公网

```powershell
hexo clean
hexo g
hexo d
```

部署完成后访问：

```text
https://jakecorina4381-create.github.io
```

如果页面没有立即更新，可以等待 1 到 3 分钟，并使用 `Ctrl + F5` 强制刷新浏览器缓存。

## 内容规划

后续计划持续更新以下方向：

* 每周 AI 新闻周报
* 每周 GitHub 热门项目推荐
* Obsidian 自动化写作流程
* Codex 辅助博客发布实践
* Hexo 主题与页面优化
* 个人学习笔记整理
* 旅行与摄影内容归档

## 维护说明

常用本地路径：

```text
Hexo 根目录：
D:\下载\hexo\blog

文章目录：
D:\下载\hexo\blog\source\_posts

图片目录：
D:\下载\hexo\blog\source\images
```

常用命令：

```powershell
hexo clean
hexo g
hexo s
hexo d
```

说明：

* `hexo clean`：清理旧的生成文件
* `hexo g`：重新生成静态网页
* `hexo s`：本地预览
* `hexo d`：部署到 GitHub Pages

## 项目目标

这个项目的长期目标是建立一个稳定、可持续的个人知识发布系统，让 Obsidian 中的内容能够经过整理后沉淀为公开博客文章。

它既是我的个人博客，也是我整理学习、记录 AI 动态、追踪开源项目和沉淀生活内容的长期小站。

## License

本仓库主要用于个人博客内容管理与展示。

除特别说明外，博客文章内容版权归作者所有，转载请注明出处。
