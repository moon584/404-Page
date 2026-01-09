# 404-Page

一个简单优雅、可定制的 404 错误页。适用于个人/团队网站、博客或任意静态站点，当用户访问不存在的链接时，提供友好的引导与返回路径。

> 技术栈占比：JavaScript 42.9% · CSS 35.2% · HTML 21.9%

## 预览

- 在线预览（GitHub Pages，启用后生效）：`https://moon584.github.io/404-Page/`
- 或者在本地直接打开 `404.html` / `index.html`

请将你提供的预览图保存为仓库根目录的 `screenshot.png`，README 中将自动显示：

![预览图](./screenshot.png)

界面要点（基于预览图）：
- 居中醒目的 “404” 标识与中文提示文案（可自定义）
- 返回首页的按钮（颜色与链接可配置）
- 渐变色背景 + 粒子/节点连线的动效背景
- 左下角音效开关按钮（可选）

## 功能特性

- 纯前端静态页面，开箱即用，无需后端
- 自适应布局，移动端与桌面端均有良好体验
- 可配置标题、副文案、按钮文本与跳转链接
- 支持插画/背景图、动画、可选的音效开关与暗色模式
- 易于集成到 GitHub Pages、Vercel、Netlify 或任意静态托管平台

## 快速开始

### 方式一：作为 GitHub Pages 的 404 页面

1. 打开仓库 Settings → Pages，启用 GitHub Pages
2. 将 `404.html` 放在 Pages 的发布根目录（仓库根目录或 `docs/`）
3. 部署完成后访问任意不存在的路径验证：
   - 例如：`https://<你的用户名>.github.io/<你的仓库名>/this-page-does-not-exist`

> 若使用 `docs/` 作为发布源，请把 `404.html` 放到 `docs/`。

### 方式二：任意静态托管平台

- 上传整个项目到 Vercel / Netlify / Nginx / Apache 等
- 基本配置：
  - Nginx：`error_page 404 /404.html;`
  - Apache（.htaccess）：`ErrorDocument 404 /404.html`
  - Vercel/Netlify：在面板中将 404 路由指向 `404.html`

### 方式三：本地预览

- 直接双击 `index.html` 或 `404.html`
- 或使用本地静态服务避免跨域限制：

```
# Python 3
python -m http.server 5173
# 浏览器访问 http://localhost:5173
```

```
# Node.js
npx serve .
# 或
npx http-server .
```

## 自定义指南

- 文案与按钮
  - 在 HTML 中修改主标题、副标题、按钮文本与按钮跳转链接（返回首页）
- 配色与主题
  - 在 CSS 中调整主色、背景渐变、按钮��色，及暗色模式（如 `prefers-color-scheme`）
- 动效与粒子背景
  - 在 CSS/JS 中开关或调节粒子数量、连接线粗细/透明度、动画时长等
- 字体与图标
  - 在 `<head>` 中引入自定义字体（本地或 Google Fonts），以及 favicon
- 声音/静音开关（可选）
  - 如需保留音效，请在 JS 中绑定左下角的控制按钮；不需要则可在 HTML 中移除该元素

## 目录结构（示例）

```
.
├── 404.html        # 404 错误页（GitHub Pages 会自动使用）
├── index.html      # 可作为独立预览入口
├── screenshot.png  # 预览图
├── assets/         # 图片/图标/插画等资源
├── css/
│   └── style.css   # 样式文件
└── js/
    └── main.js     # 基础交互/动画脚本
```

实际结构以仓库为准。

## 技术栈

- HTML：语义化结构与基础内容
- CSS：响应式布局、主题配色与动画
- JavaScript：交互逻辑、按钮行为、粒子背景与可选音效

> 本仓库的语言占比（GitHub 统计）：JavaScript 42.9%，CSS 35.2%，HTML 21.9%。

## 无障碍与最佳实践

- 为图像提供 `alt` 文本
- 合理的对比度与可读字号
- 交互元素具备键盘可达性与焦点样式
- 提供清晰的“返回主页”按钮与导航
- 元数据与 SEO：合理的 `<title>`、`<meta>`，可选 Open Graph 标签

## 部署

- GitHub Pages
  - Settings → Pages → 选择分支与目录（root 或 docs）
  - 确保 `404.html` 位于发布根目录
- 其他平台
  - 配置 404 路由到 `404.html`
  - 建议开启 gzip/br 压缩与合理缓存（HTML 短缓存，静态资源长缓存）

## 贡献

欢迎提交 Issue 或 Pull Request：
- 修复 Bug、改进样式与交互
- 增加主题与多语言支持
- 优化无障碍与性能

提交前请确保本地预览正常与基础校验通过。
