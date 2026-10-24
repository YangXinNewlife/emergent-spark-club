# 灵感涌现 CLUB - Emergent Spark Club

品牌官网 - 支持中文/英文/法语三语切换

## 文件结构

```
├── index.html    # 主页面（包含所有 CSS 和 JavaScript）
├── logo.png      # 品牌 Logo
└── README.md     # 说明文档
```

## 部署到 GitHub Pages

### 方法 1：使用 GitHub CLI（推荐）

```bash
# 安装 GitHub CLI（如果未安装）
brew install gh

# 登录 GitHub
gh auth login

# 创建仓库并推送代码
gh repo create emergent-spark --public --source=. --remote=origin
git push -u origin main

# 启用 GitHub Pages
gh api repos/{你的用户名}/emergent-spark/pages -X POST -f "build_type=workflow"
```

### 方法 2：手动部署

1. 在 GitHub 上创建新仓库 `emergent-spark`（Public）
2. 执行以下命令：

```bash
git remote add origin https://github.com/你的用户名/emergent-spark.git
git branch -M main
git push -u origin main
```

3. 在仓库 Settings → Pages 中：
   - Source 选择 "Deploy from a branch"
   - Branch 选择 "main" / "root"
   - 点击 Save

4. 等待 1-2 分钟，访问 `https://你的用户名.github.io/emergent-spark/`

## 部署到其他服务器

### 静态托管服务

**Vercel:**
```bash
npm i -g vercel
vercel
```

**Netlify:**
```bash
# 直接拖拽文件夹到 Netlify 界面
# 或使用 CLI
npm i -g netlify-cli
netlify deploy --prod
```

**Cloudflare Pages:**
1. 登录 Cloudflare Dashboard
2. 进入 Pages → Create a project
3. 连接 GitHub 仓库或直接上传文件

### 传统服务器

将 `index.html` 和 `logo.png` 上传到 Web 服务器根目录：

```bash
# 使用 SCP
scp index.html logo.png user@yourserver.com:/var/www/html/

# 使用 FTP/SFTP
# 上传到 public_html 或 www 目录
```

## 功能特性

- ✅ 响应式设计（移动端/平板/桌面）
- ✅ 三语切换（中文/English/Français）
- ✅ 粒子网络动画背景
- ✅ 滚动动画效果
- ✅ 毛玻璃导航栏
- ✅ 活动报名跳转
- ✅ 商务合作联系信息

## 技术栈

- 纯 HTML/CSS/JavaScript（无框架依赖）
- Canvas 粒子动画
- IntersectionObserver 滚动动画
- localStorage 语言偏好保存

## 更新内容

修改 `index.html` 后，提交并推送：

```bash
git add .
git commit -m "更新内容描述"
git push
```

GitHub Pages 会自动重新部署。

## 许可证

© 2026 灵感涌现 · Emergent Spark Club. All rights reserved.
