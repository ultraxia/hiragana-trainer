# 日语五十音学习 - PWA 应用

一个支持 iOS PWA 的日语五十音（平假名）学习工具。

## 功能特性

- 📱 支持 PWA（渐进式 Web 应用）
- 🍎 完美支持 iOS 添加到主屏幕
- 📝 优化的助记方法
- 🎯 随机检查功能
- 🔄 混淆训练模式
- 📚 错题本
- 📊 学习统计

## 部署到 GitHub Pages

### 方法 1：使用 GitHub Actions 自动部署（推荐）

1. 将代码推送到 GitHub 仓库

```bash
git add .
git commit -m "Add PWA support"
git push origin main
```

2. 在 GitHub 仓库中启用 GitHub Pages：
   - 进入仓库的 `Settings` > `Pages`
   - 在 `Source` 下选择 `GitHub Actions`
   - 保存设置

3. 等待自动部署完成（通常需要 1-2 分钟）

4. 访问你的网站：`https://你的用户名.github.io/仓库名/`

### 方法 2：手动部署

1. 在 GitHub 仓库中启用 GitHub Pages：
   - 进入仓库的 `Settings` > `Pages`
   - 在 `Source` 下选择 `Deploy from a branch`
   - 选择 `main` 分支和 `/ (root)` 文件夹
   - 点击 `Save`

2. 等待部署完成

3. 访问你的网站：`https://你的用户名.github.io/仓库名/`

## 生成 PWA 图标

项目需要图标才能完整支持 PWA。有以下几种方式：

### 方式 1：使用提供的图标生成器（最简单）

1. 在浏览器中打开 `icons/generate-icon.html`
2. 点击"生成所有图标"按钮
3. 图标会自动下载到你的下载文件夹
4. 将下载的所有图标文件移动到 `icons/` 目录

### 方式 2：使用在线工具

1. 访问 [RealFaviconGenerator](https://realfavicongenerator.net/) 或 [PWA Builder](https://www.pwabuilder.com/imageGenerator)
2. 上传你的图标（建议 512x512 PNG）
3. 下载生成的图标包
4. 将图标文件放入 `icons/` 目录

### 方式 3：使用命令行工具

查看 `icons/README.md` 获取详细说明。

## 在 iOS 设备上安装 PWA

1. 在 Safari 浏览器中打开网站
2. 点击底部的分享按钮 📤
3. 滚动找到"添加到主屏幕"
4. 点击"添加"

现在你可以从主屏幕启动应用，它会像原生应用一样全屏运行！

## 在 Android 设备上安装 PWA

1. 在 Chrome 浏览器中打开网站
2. 点击右上角的菜单（三个点）
3. 选择"添加到主屏幕"或"安装应用"
4. 点击"安装"

## 技术栈

- 纯 HTML/CSS/JavaScript
- Service Worker（离线支持）
- Web App Manifest（PWA 配置）
- LocalStorage（数据持久化）

## 本地开发

直接用浏览器打开 `index.html` 即可。

如果需要测试 Service Worker，建议使用本地服务器：

```bash
# 使用 Python
python -m http.server 8000

# 或使用 Node.js
npx serve

# 或使用 PHP
php -S localhost:8000
```

然后访问 `http://localhost:8000`

## 故障排除

### PWA 无法安装

1. 确保网站通过 HTTPS 访问（GitHub Pages 默认支持）
2. 确保所有图标文件都已正确放置
3. 检查浏览器控制台是否有错误
4. 清除浏览器缓存后重试

### Service Worker 不工作

1. 打开浏览器开发者工具
2. 进入 Application/应用 标签
3. 查看 Service Workers 部分
4. 点击 "Unregister" 注销旧的 Service Worker
5. 刷新页面重新注册

### iOS 图标不显示

1. 确保 `apple-touch-icon` 文件存在
2. 图标必须是 PNG 格式
3. 建议尺寸为 180x180 像素
4. 从主屏幕删除应用后重新添加

## 许可证

MIT License

## 贡献

欢迎提交 Issue 和 Pull Request！
