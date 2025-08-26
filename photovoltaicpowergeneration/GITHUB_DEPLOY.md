# GitHub Pages 部署指南

## 🚀 部署步骤

### 1. 创建GitHub仓库
1. 在GitHub上创建新的仓库
2. 仓库名称建议：`solar-power-dashboard` 或 `川奇光伏发电看板`

### 2. 上传文件
将以下文件上传到仓库根目录：
```
├── login.html          # 登录页面（入口页面）
├── index.html          # 主看板页面
├── echarts.min.js      # 图表库
├── 厂房照片.jpg        # 现场照片
├── 二氧化碳.png        # CO₂减排图标
├── 森林.png            # 等效植树图标
├── 煤.png              # 节约标准煤图标
├── README.md           # 项目说明
└── GITHUB_DEPLOY.md    # 本部署指南
```

### 3. 启用GitHub Pages
1. 进入仓库设置 (Settings)
2. 找到 "Pages" 选项
3. 在 "Source" 中选择 "Deploy from a branch"
4. 选择 "main" 分支和 "/ (root)" 文件夹
5. 点击 "Save"

### 4. 设置入口页面
GitHub Pages 默认会寻找 `index.html`，但我们需要 `login.html` 作为入口：
- 方法1：将 `login.html` 重命名为 `index.html`，原 `index.html` 重命名为 `dashboard.html`
- 方法2：在仓库根目录创建 `.nojekyll` 文件，并设置 `login.html` 为默认页面

## 🔐 密码保护说明

### 访问密码
- **密码**: `josun888`
- **有效期**: 24小时（登录后24小时内无需重新输入密码）

### 安全特性
- ✅ 纯前端密码验证
- ✅ 本地存储认证状态
- ✅ 24小时自动过期
- ✅ 支持回车键快速登录
- ✅ 错误提示和加载状态

## 🌐 访问方式

部署完成后，您的看板将通过以下地址访问：
```
https://[用户名].github.io/[仓库名]/
```

例如：
```
https://yourusername.github.io/solar-power-dashboard/
```

## 📱 兼容性

- ✅ 现代浏览器 (Chrome, Firefox, Safari, Edge)
- ✅ 移动设备响应式设计
- ✅ 完全离线运行
- ✅ 无需后端服务器

## 🔧 自定义配置

### 修改密码
在 `login.html` 文件中找到以下代码并修改：
```javascript
if (password === 'josun888') {
    // 将 'josun888' 改为您的新密码
}
```

### 修改有效期
在 `login.html` 和 `index.html` 中找到以下代码并修改：
```javascript
if (hoursDiff < 24) {
    // 将 24 改为您希望的小时数
}
```

## ⚠️ 注意事项

1. **密码安全**: 密码是明文存储在前端代码中的，请谨慎使用
2. **访问控制**: 任何人都可以查看源代码，包括密码
3. **建议用途**: 适用于内部团队或非敏感数据的展示
4. **定期更新**: 建议定期更换密码

## 🆘 故障排除

### 页面无法访问
- 检查GitHub Pages是否已启用
- 确认文件路径正确
- 等待几分钟让GitHub Pages生效

### 密码验证失败
- 确认密码输入正确：`josun888`
- 检查浏览器是否支持localStorage
- 清除浏览器缓存后重试

### 图表无法显示
- 确认 `echarts.min.js` 文件已上传
- 检查浏览器控制台是否有错误信息

## 📞 技术支持

如遇到问题，请检查：
1. GitHub Pages 部署状态
2. 浏览器控制台错误信息
3. 文件是否完整上传

---

*部署完成后，您的光伏发电看板将具备完整的密码保护功能！* 