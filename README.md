# 微信分享卡片 📱

基于GitHub Pages的微信分享卡片系统，支持动态加载和微信分享功能。

## 🌐 在线演示

- **主页面**: [https://tianyu365.github.io/wxkpzdy/](https://tianyu365.github.io/wxkpzdy/)
- **测试页面**: [https://tianyu365.github.io/wxkpzdy/test.html](https://tianyu365.github.io/wxkpzdy/test.html)
- **分享示例**: [https://tianyu365.github.io/wxkpzdy/?sid=123456](https://tianyu365.github.io/wxkpzdy/?sid=123456)

## 🚀 快速开始

### 1. 访问分享卡片
```
https://tianyu365.github.io/wxkpzdy/?sid=你的分享ID
```

### 2. 创建分享卡片
访问 [https://wx.wxshpt.shop/creat.html](https://wx.wxshpt.shop/creat.html) 创建新的分享卡片

## 📁 项目结构

```
wxkpzdy/
├── index.html              # 主页面
├── test.html               # 测试页面
├── _config.yml             # Jekyll配置
├── .github/
│   └── workflows/
│       └── pages.yml       # 自动部署
└── README.md               # 说明文档
```

## 🔧 技术特性

- ✅ **响应式设计** - 支持手机和桌面端
- ✅ **微信分享** - 完整的微信JS-SDK集成
- ✅ **动态加载** - 通过API获取卡片信息
- ✅ **二维码生成** - 自动生成分享二维码
- ✅ **自动部署** - GitHub Actions自动部署
- ✅ **SEO优化** - Jekyll SEO插件支持

## 🛠️ 部署说明

### GitHub Pages部署

1. Fork本仓库
2. 启用GitHub Pages功能
3. 设置Pages源为GitHub Actions
4. 自动部署完成

### 服务器API部署

将 `admin/` 目录上传到服务器，确保以下API可访问：
- `get_share.php` - 获取分享卡片信息
- `get_signature.php` - 获取微信签名
- `redirect.php` - 重定向页面

## 📱 使用方式

### 创建分享卡片
1. 访问创建页面
2. 填写卡片信息（标题、描述、图片、链接）
3. 获取分享ID

### 分享卡片
1. 使用分享链接：`https://tianyu365.github.io/wxkpzdy/?sid=分享ID`
2. 在微信中打开链接
3. 点击右上角分享按钮

## 🔍 API接口

### 获取分享卡片
```http
GET /admin/get_share.php?sid={分享ID}
```

### 获取微信签名
```http
GET /admin/get_signature.php?url={当前页面URL}
```

## 🎯 配置要求

- **服务器**: PHP 7.0+ + MySQL 5.7+
- **域名**: 需要在微信公众平台配置JS安全域名
- **HTTPS**: 建议使用HTTPS协议

## 📄 许可证

MIT License

## 🤝 贡献

欢迎提交Issue和Pull Request！

## 📞 联系

- GitHub: [@tianyu365](https://github.com/tianyu365)
- 项目地址: [https://github.com/tianyu365/wxkpzdy](https://github.com/tianyu365/wxkpzdy)
