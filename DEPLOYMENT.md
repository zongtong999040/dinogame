# 🦖 恐龙生存游戏 - GitHub Pages 部署说明

## 🌐 在线访问

游戏已部署到GitHub Pages，访问地址：
**https://zongtong999040.github.io/dinogame/**

## 📋 手动启用GitHub Pages步骤

如果GitHub Pages还没有自动启用，请按照以下步骤操作：

### 方法1: 通过GitHub网页设置（推荐）

1. 访问仓库设置页面：
   https://github.com/zongtong999040/dinogame/settings/pages

2. 在"Source"部分：
   - 选择分支：`gh-pages`
   - 选择文件夹：`/ (root)`

3. 点击"Save"按钮

4. 等待几秒钟，页面会刷新并显示：
   - ✅ Your site is live at https://zongtong999040.github.io/dinogame/

### 方法2: 使用GitHub CLI（如果已安装）

```bash
# 安装GitHub CLI（如果还没有）
# macOS: brew install gh
# Linux: sudo apt install gh
# Windows: scoop install gh

# 登录GitHub
gh auth login

# 启用GitHub Pages
gh api \
  --method POST \
  -H "Accept: application/vnd.github.v3+json" \
  /repos/zongtong999040/dinogame/pages \
  -f source='{"branch":"gh-pages","path":"/"}'
```

## 🔄 自动部署

项目已配置GitHub Actions工作流，每次推送到master分支时会自动更新gh-pages分支：

- 工作流文件：`.github/workflows/deploy.yml`
- 触发条件：推送到master分支
- 部署目标：gh-pages分支

## 📦 项目结构

```
dinogame/
├── index.html              # 游戏主文件
├── .github/
│   └── workflows/
│       └── deploy.yml      # 自动部署工作流
├── ENEMY_GUIDE.md          # 敌人图鉴
├── BATTLE_ATTACK_CHANGE_TEST.md  # 测试文档
└── README.md              # 本文件
```

## 🎮 游戏特性

- ✅ 多种恐龙选择（霸王龙、三角龙、剑龙等）
- ✅ 三个探索区域（森林、河流、竞技场）
- ✅ 17种不同的敌对生物
- ✅ 战斗中切换攻击方式
- ✅ 鼠标点击移动
- ✅ 成长系统（幼年→成年）
- ✅ 肉类收集和水分管理

## 🛠️ 技术栈

- 纯HTML5 + CSS3 + JavaScript
- Tailwind CSS（通过CDN）
- Font Awesome图标
- 响应式设计

## 📝 更新日志

### 最新更新
- 添加17种不同的敌对生物
- 战斗中可以切换攻击方式
- 添加鼠标点击移动功能
- 优化UI和动画效果

## 🐛 问题反馈

如果遇到问题，请在GitHub上提issue：
https://github.com/zongtong999040/dinogame/issues

## 📄 许可证

本项目仅供学习和娱乐使用。
