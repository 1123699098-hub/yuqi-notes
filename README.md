# YUQI · 让万物穿过

个人知识管理工具。随手摘录、记录思考、长记精华 —— 全部归位，井然有序。

## 功能

### 三大板块
- **摘抄** — 从阅读中收集的金句、段落与灵感，支持来源、类别、Author、Title 标签
- **记录** — 日常的思考、想法与备忘，支持活动标签
- **长记** — 更长的思考、创作、感受

### 时间维度筛选
DAY / WEEK / MONTH / YEAR 切换，快速回顾不同时间范围的内容

### 详情页矩阵展示
- 首页预览 → 点击标题进入详情页
- 3×5 矩阵排列，支持来源/类别/作者/活动多维度筛选
- AI 分析功能（支持配置个人 API Key）

### AI 分析
- 点击详情页右上角 **AI 分析** → 点击 **⚙️ 设置** → 输入你的 Kimi API Key
- 配置保存在浏览器本地，刷新不丢失
- 支持 moonshot-v1-8k / 32k / 128k 模型切换
- 未配置时，可用「复制 Prompt」粘贴到 Kimi / ChatGPT 提问

## 部署到 GitHub Pages

### 1. 创建 GitHub 仓库
- 访问 [github.com/new](https://github.com/new)
- 仓库名：`yuqi-notes`
- 选择 **Public**（Public 才能免费使用 GitHub Pages）
- 点击 **Create repository**

### 2. 上传文件
将本文件夹内的所有文件上传到仓库的 **main** 分支根目录。

**方式 A：网页上传（最简单）**
- 进入新创建的仓库
- 点击 **"uploading an existing file"**
- 拖拽 `index.html` 到上传区域
- 点击 **Commit changes**

**方式 B：命令行推送**
```bash
cd yuqi-notes-deploy
git init
git add index.html README.md .gitignore
git commit -m "feat: add YUQI note app"
git branch -M main
git remote add origin https://github.com/你的用户名/yuqi-notes.git
git push -u origin main
```

### 3. 开启 GitHub Pages
- 仓库 → **Settings** → **Pages**
- **Branch** 选择 `main` / `(root)` → **Save**
- 等待 1-2 分钟，刷新即可看到链接：
  ```
  https://你的用户名.github.io/yuqi-notes
  ```

### 4. 完成
打开链接即可使用。

---

## 使用提示

- **数据存储**：所有内容保存在浏览器 `localStorage` 中，换浏览器或清除缓存会丢失
- **AI 配置**：API Key 仅保存在本地，不会上传到任何服务器
- **快捷键**：输入框内按 `⌘ Enter` / `Ctrl Enter` 快速提交
- **备份**：建议定期导出 `localStorage` 中的 `quicknote_data` 和 `yuqi_api_config`

## 文件说明

| 文件 | 说明 |
|------|------|
| `index.html` | 单文件应用，包含所有样式和逻辑 |
| `.gitignore` | 忽略系统文件 |
| `README.md` | 本说明文档 |
