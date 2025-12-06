# PWA 图标说明

这个目录需要包含 PWA 应用的图标文件。

## 需要的图标尺寸

请准备以下尺寸的 PNG 图标：

- `icon-16x16.png` - 16x16 像素（网站 favicon）
- `icon-32x32.png` - 32x32 像素（网站 favicon）
- `icon-72x72.png` - 72x72 像素
- `icon-96x96.png` - 96x96 像素
- `icon-120x120.png` - 120x120 像素（iOS）
- `icon-128x128.png` - 128x128 像素
- `icon-144x144.png` - 144x144 像素
- `icon-152x152.png` - 152x152 像素（iOS）
- `icon-180x180.png` - 180x180 像素（iOS）
- `icon-192x192.png` - 192x192 像素（Android）
- `icon-384x384.png` - 384x384 像素
- `icon-512x512.png` - 512x512 像素（Android、启动画面）

## 如何生成图标

### 方法 1：使用在线工具

推荐使用 [RealFaviconGenerator](https://realfavicongenerator.net/) 或 [PWA Asset Generator](https://www.pwabuilder.com/imageGenerator)

1. 访问网站
2. 上传你的原始图标（建议 512x512 或更大）
3. 下载生成的所有尺寸图标
4. 将图标文件放入此 `icons` 目录

### 方法 2：使用命令行工具

使用 ImageMagick 批量生成：

```bash
# 安装 ImageMagick
brew install imagemagick  # macOS
# 或 sudo apt-get install imagemagick  # Linux

# 从原始图标生成所有尺寸
convert source.png -resize 16x16 icon-16x16.png
convert source.png -resize 32x32 icon-32x32.png
convert source.png -resize 72x72 icon-72x72.png
convert source.png -resize 96x96 icon-96x96.png
convert source.png -resize 120x120 icon-120x120.png
convert source.png -resize 128x128 icon-128x128.png
convert source.png -resize 144x144 icon-144x144.png
convert source.png -resize 152x152 icon-152x152.png
convert source.png -resize 180x180 icon-180x180.png
convert source.png -resize 192x192 icon-192x192.png
convert source.png -resize 384x384 icon-384x384.png
convert source.png -resize 512x512 icon-512x512.png
```

### 方法 3：使用 npm 工具

```bash
npm install -g pwa-asset-generator
pwa-asset-generator source.png icons -m manifest.json
```

## 图标设计建议

- 使用简单、清晰的设计
- 确保在小尺寸下仍然清晰可辨
- 使用方形画布（1:1 比例）
- 对于 iOS，边缘会自动添加圆角
- 对于 Android maskable icons，确保重要内容在安全区域内（中心 80%）

## 临时替代方案

如果暂时没有图标，可以：
1. 使用简单的纯色背景 + 文字（如"あ"）
2. 使用在线生成器快速创建占位图标
3. 稍后再替换为正式设计的图标
