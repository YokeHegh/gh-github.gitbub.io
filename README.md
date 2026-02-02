# 部署指南：过年倒计时页面到GitHub Pages

## 概述

您的过年倒计时页面已准备就绪，可以部署到GitHub Pages。部署后，您将获得一个可直接点击访问的永久链接：`https://yourusername.github.io`

## 部署步骤

### 第一步：创建GitHub账户（如果还没有）

如果您还没有GitHub账户，请访问 [https://github.com](https://github.com) 注册一个免费账户。

### 第二步：创建仓库

1. 登录GitHub后，点击右上角的 "+" 号，选择 "New repository"
2. 在仓库名称框中输入：`yourusername.github.io` （将 `yourusername` 替换为您的实际GitHub用户名）
3. 选择 "Public" 使仓库公开
4. **不要**勾选 "Initialize this repository with a README"
5. 点击 "Create repository" 按钮

### 第三步：上传文件

有几种方式上传文件到您的仓库：

#### 方式一：网页上传（推荐新手）
1. 在仓库页面，点击 "Add file" 下拉菜单，选择 "Upload files"
2. 将以下文件从您的计算机拖拽到上传区域：
   - `index.html`
   - `style.css` (如果有)
   - `script.js` (如果有)
   - **`music.mp3`** (您下载并重命名的音乐文件)
3. 在 "Commit changes" 区域输入提交信息，例如 "Upload project files"
4. 点击 "Commit changes" 按钮

#### 关于背景音乐的重要说明
由于代码中引用了本地音乐文件，**您必须手动上传音乐文件**才能听到声音：
1. 下载您喜欢的《拜新年》MP3音乐。
2. 将其重命名为 **`music.mp3`**。
3. 按照上述“网页上传”步骤，将其上传到仓库的**根目录**（和 `index.html` 在一起）。

#### 方式二：使用命令行
```bash
# 克隆仓库到本地
git clone https://github.com/yourusername/yourusername.github.io.git
cd yourusername.github.io

# 复制所有项目文件（包括 index.html 和 music.mp3）到此目录
# 然后添加和提交更改
git add .
git commit -m "Initial commit with music"
git push origin main
```

### 第四步：启用GitHub Pages

1. 在仓库页面，点击顶部的 "Settings" 选项卡
2. 向下滚动到 "Pages" 部分（在左侧边栏也可能找到）
3. 在 "Source" 部分，从下拉菜单中选择 "Deploy from a branch"
4. 选择 "main" 分支和 "/root" 文件夹
5. 点击 "Save" 按钮
6. 等待页面自动刷新

### 第五步：访问您的网站

- 等待几分钟让GitHub Pages构建您的网站
- 访问 `https://yourusername.github.io` 即可看到您的倒计时页面
- 此链接可直接分享给他人，点击即可访问

## 重要提示

- GitHub Pages需要一些时间来部署（通常1-5分钟）
- 确保仓库名称是 `yourusername.github.io` 的格式，否则GitHub Pages不会自动启用
- 如果您看到 "Page not found" 错误，请检查分支名称是否为 "main" 或 "master"
- 您可以在仓库的 "Settings" -> "Pages" 部分查看部署状态

## 更新网站

如果您想更新网站内容：
1. 上传更新后的 `index.html` 文件
2. GitHub Pages会自动检测更改并重新部署
3. 刷新 `https://yourusername.github.io` 查看更新

## 故障排除

如果遇到问题：
- 确认仓库名称正确：`yourusername.github.io`
- 确认 `index.html` 文件在仓库根目录
- 确认已在 Settings -> Pages 中启用了GitHub Pages
- 检查是否选择了正确的分支（通常是 main 或 master）

---

您的过年倒计时页面现在具备以下功能：
- 年:月:日:时 分:秒:毫秒的完整倒计时
- 自动播放《拜新年》背景音乐
- 喜庆的视觉效果和动画
- 移动端友好设计
