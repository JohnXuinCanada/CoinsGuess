# 上传猜硬币游戏到 GitHub 的完整指南

## ⚠️ 安全第一
**重要：** 你的 Personal Access Token 已经在对话中泄露，请先到 GitHub 删除旧 Token 并生成新的！

## 📋 准备工作

### 1. 安装 Git
如果还没安装 Git，先安装：
- **Windows**: 下载 https://git-scm.com/download/win
- **Mac**: 打开终端，输入 `git --version`（会自动提示安装）
- **Linux**: `sudo apt-get install git`

### 2. 配置 Git（首次使用）
```bash
git config --global user.name "JohnXuinCanada"
git config --global user.email "JohnXuinCanada@gmail.com"
```

## 🚀 上传步骤

### 步骤 1: 在 GitHub 创建仓库
1. 登录 GitHub.com
2. 点击右上角 "+" → "New repository"
3. 仓库名称：`CoinsGuess`
4. 描述（可选）：`双人猜硬币对战游戏`
5. 选择 **Public**（公开，这样才能用 GitHub Pages）
6. **不要** 勾选 "Add a README file"
7. 点击 "Create repository"

### 步骤 2: 在本地准备文件
1. 创建一个新文件夹，命名为 `CoinsGuess`
2. 将 `coin-guess-game.html` 文件放入这个文件夹
3. **重命名文件**为 `index.html`（这样 GitHub Pages 会自动识别）

### 步骤 3: 上传代码
打开终端/命令提示符，切换到 `CoinsGuess` 文件夹，然后执行：

```bash
# 初始化 Git 仓库
git init

# 添加文件
git add index.html

# 提交
git commit -m "初始版本：双人猜硬币游戏"

# 设置主分支名称
git branch -M main

# 连接到 GitHub 仓库
git remote add origin https://github.com/JohnXuinCanada/CoinsGuess.git

# 推送代码（会要求输入用户名和密码）
# 用户名：JohnXuinCanada
# 密码：你的新 Personal Access Token（不是 GitHub 密码！）
git push -u origin main
```

### 步骤 4: 启用 GitHub Pages
1. 在 GitHub 仓库页面，点击 "Settings"
2. 左侧菜单找到 "Pages"
3. 在 "Source" 下拉菜单选择 "main" 分支
4. 点击 "Save"
5. 等待 1-2 分钟

### 步骤 5: 获取分享链接
几分钟后，你的游戏就可以通过以下链接访问了：

🎮 **游戏链接：**
```
https://johnxuincanada.github.io/CoinsGuess/
```

把这个链接发给朋友，他们就可以在手机或电脑上直接玩了！

## 🔄 更新游戏（以后修改代码后）

```bash
# 1. 修改 index.html 文件
# 2. 保存后，在终端执行：

git add index.html
git commit -m "更新游戏"
git push
```

等待 1-2 分钟后，网站会自动更新。

## 🎯 快速命令版本（一键复制）

```bash
# 在 CoinsGuess 文件夹中执行：
git init
git add index.html
git commit -m "初始版本：双人猜硬币游戏"
git branch -M main
git remote add origin https://github.com/JohnXuinCanada/CoinsGuess.git
git push -u origin main
```

## ❓ 常见问题

### Q: 推送时要求输入密码？
A: 密码框输入你的 **Personal Access Token**，不是 GitHub 账号密码！

### Q: 网站显示 404？
A: 等待 1-2 分钟，GitHub Pages 需要时间部署。

### Q: 想修改游戏怎么办？
A: 修改 `index.html` 文件，然后重新 `git add`、`commit`、`push`。

### Q: Token 还是不安全？
A: 使用 Git Credential Manager 存储 Token，避免每次输入。

## 📱 分享给朋友

直接把这个链接发给朋友：
```
https://johnxuincanada.github.io/CoinsGuess/
```

他们可以：
- 在手机浏览器打开
- 在电脑浏览器打开
- 添加到主屏幕（手机）当作 App 使用

---

**祝你游戏愉快！** 🎮
