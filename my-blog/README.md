# Hexo 博客

这是一个使用 Hexo 框架创建的博客网站。

## 项目结构

- `source/_posts/`: 存放博客文章的目录
- `themes/`: 存放主题的目录
- `public/`: 生成的静态文件目录
- `_config.yml`: 网站配置文件

## 使用说明

### 安装依赖

```bash
npm install
```

### 创建新文章

```bash
npx hexo new "文章标题"
```

这将在 `source/_posts/` 目录下创建一个新的 Markdown 文件。

### 生成静态文件

```bash
npx hexo generate
# 或者使用简写
npx hexo g
```

### 启动本地服务器

```bash
npx hexo server
# 或者使用简写
npx hexo s
```

访问 `http://localhost:4000` 预览您的网站。

### 部署网站

首先，需要安装部署插件：

```bash
npm install hexo-deployer-git --save
```

然后，修改 `_config.yml` 文件中的部署配置：

```yaml
deploy:
  type: git
  repo: <您的 GitHub 仓库地址>
  branch: [部署的分支]
```

最后，运行部署命令：

```bash
npx hexo deploy
# 或者使用简写
npx hexo d
```

### 清理

```bash
npx hexo clean
```

## 自定义配置

### 修改网站信息

编辑 `_config.yml` 文件，修改以下内容：

```yaml
# Site
title: 您的网站标题
subtitle: 副标题
description: 网站描述
keywords: 关键词
author: 您的名字
language: zh-CN
timezone: Asia/Shanghai
```

### 更换主题

1. 在 `themes/` 目录下克隆主题仓库
2. 修改 `_config.yml` 文件中的 `theme` 字段为主题名称

## 常见问题解决

如果遇到服务器启动问题，可以尝试以下步骤：

1. 清理缓存：`npx hexo clean`
2. 重新生成静态文件：`npx hexo generate`
3. 重启服务器：`npx hexo server`

## 更多资源

- [Hexo 官方文档](https://hexo.io/zh-cn/docs/)
- [Hexo 主题](https://hexo.io/themes/)
- [Hexo GitHub](https://github.com/hexojs/hexo)