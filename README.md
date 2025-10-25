# 微信分享卡片 - GitHub Pages版本

这是一个基于GitHub Pages的微信分享卡片系统，通过JavaScript调用远程API来获取数据。

## 项目结构

```
github-pages/
├── index.html              # GitHub Pages主页面
├── admin/                  # 服务器API目录
│   ├── get_share.php       # 获取分享卡片API
│   ├── get_signature.php   # 获取微信签名API
│   ├── redirect.php        # 重定向页面
│   └── db_config.php       # 数据库配置
└── README.md               # 说明文档
```

## 部署步骤

### 1. GitHub Pages部署

1. 将 `index.html` 上传到GitHub仓库
2. 启用GitHub Pages功能
3. 设置Pages源为main分支
4. 访问 `https://your-username.github.io/your-repo/`

### 2. 服务器API部署

1. 将 `admin/` 目录上传到你的服务器
2. 配置数据库连接信息（修改 `db_config.php`）
3. 确保服务器支持PHP和MySQL
4. 设置CORS允许跨域访问

### 3. 配置修改

#### 修改API地址
在 `index.html` 中修改API地址：
```javascript
const API_BASE_URL = 'https://your-server-domain.com/admin';
```

#### 修改微信配置
在 `index.html` 中修改微信AppID：
```javascript
appId: 'your_app_id', // 替换为你的微信AppID
```

#### 修改数据库配置
在 `admin/db_config.php` 中修改数据库信息：
```php
$db_url = "localhost";
$db_user = "your_db_user";
$db_pwd = "your_db_password";
$db_name = "your_db_name";
$appid = "your_wechat_appid";
$appsecret = "your_wechat_appsecret";
```

## API接口说明

### 获取分享卡片信息
- **URL**: `/admin/get_share.php?sid={分享ID}`
- **方法**: GET
- **返回**: JSON格式的卡片信息

### 获取微信签名
- **URL**: `/admin/get_signature.php?url={当前页面URL}`
- **方法**: GET
- **返回**: JSON格式的微信JS-SDK签名信息

### 重定向页面
- **URL**: `/admin/redirect.php?sid={分享ID}`
- **方法**: GET
- **功能**: 重定向到目标链接

## 使用说明

1. 访问GitHub Pages页面
2. 在URL后添加 `?sid=分享ID` 参数
3. 页面会自动加载并显示分享卡片
4. 支持微信分享功能

## 注意事项

1. 确保服务器支持CORS跨域访问
2. 微信分享需要在微信公众平台配置JS安全域名
3. 数据库表结构需要与原有系统保持一致
4. 建议使用HTTPS协议确保安全性

## 技术栈

- **前端**: HTML5, CSS3, JavaScript (ES6+)
- **后端**: PHP 7.0+
- **数据库**: MySQL 5.7+
- **部署**: GitHub Pages + 独立服务器
