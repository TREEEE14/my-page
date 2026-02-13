# TREE 个人主页

简约且高级的个人主页，展示教育背景、实习经历和技能专长。

## 功能特点

- 🎨 简约现代的设计风格
- 📱 完全响应式布局，支持移动端
- ✨ 流畅的动画效果
- 🚀 快速加载，性能优化
- ♿ 良好的可访问性

## 部署到 GitHub Pages

### 方法一：使用 GitHub Pages（推荐）

1. **创建 GitHub 仓库**
   - 在 GitHub 上创建一个新仓库（例如：`my-personal-page`）
   - 将仓库设置为公开（Public）

2. **上传文件**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/你的用户名/my-personal-page.git
   git push -u origin main
   ```

3. **启用 GitHub Pages**
   - 进入仓库的 Settings（设置）
   - 找到 Pages 选项
   - 在 Source 中选择 `main` 分支
   - 选择 `/ (root)` 文件夹
   - 点击 Save

4. **访问你的网站**
   - 几分钟后，你的网站将在 `https://你的用户名.github.io/my-personal-page` 可用

### 方法二：使用 GitHub Actions 自动部署

创建 `.github/workflows/deploy.yml` 文件：

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches:
      - main

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./
```

## 自定义内容

### 修改个人信息

编辑 `index.html` 文件，更新以下内容：
- 姓名（TREE）
- 教育背景
- 实习经历
- 技能标签
- 联系方式（GitHub、邮箱等）

### 修改样式

编辑 `styles.css` 文件，可以调整：
- 颜色主题（`:root` 变量）
- 字体大小和间距
- 动画效果

### 添加新内容

可以在 `index.html` 中添加新的 section，例如：
- 项目展示
- 博客文章
- 证书和奖项
- 个人作品集

## 文件结构

```
MyWebPage/
├── index.html      # 主页面
├── styles.css      # 样式文件
├── script.js       # 交互脚本
└── README.md       # 说明文档
```

## 浏览器支持

- Chrome（最新版）
- Firefox（最新版）
- Safari（最新版）
- Edge（最新版）

## 许可证

MIT License

## 联系方式

如有问题或建议，欢迎通过 GitHub Issues 联系。
