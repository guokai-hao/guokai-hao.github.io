# 学术个人主页模板（Not Pure Poole Academic Edition）

这是基于 **Not Pure Poole** 改造的“学术简历式个人主页”。已经删除博客文章流，首页改为：

**左侧：头像 / 姓名 / 身份 / 学校 / 地点 / 邮箱 / 学术链接**  
**右侧：About Me → Research Interests → Publications → Research Overview（PDF逐页平铺）**

---

## 你主要只需要改 5 个地方

### 1. `_data/profile.yml`
修改：
- 姓名
- Ph.D. Student / 身份
- 学校
- 地点
- 邮箱
- About Me
- 研究汇报 PDF 文件名

如果你现有文件就叫 `CV.pdf`，保持：

```yaml
research_overview:
  file: "/CV.pdf"
```

### 2. `_data/research.yml`
修改你的研究方向。

### 3. `_data/publications.yml`
填写你的论文信息。每增加一篇论文，就复制一个完整的 `- year:` 块。

### 4. `_data/social.yml`
把 Google Scholar / ORCID / GitHub / Email 改成你的链接。

### 5. `_config.yml`
至少修改：

```yaml
title: "你的名字"
description: "Ph.D. Student | Reinforcement Learning"
url: "https://guokai-hao.github.io"
author:
  name: "你的名字"
  email: "你的邮箱"
```

---

## 头像怎么换？

把你的头像上传到仓库，例如命名为：

`profile.jpg`

然后把 `_config.yml` 改成：

```yaml
avatar: /profile.jpg
```

---

## CV.pdf / 研究PPT怎么放？

本 ZIP **没有包含你的私人 PDF**。

你 GitHub 仓库里已经有 `CV.pdf` 的话，保留它即可。

本模板会使用 PDF.js 将 PDF **逐页直接铺在网页中**，不会出现 iframe 小窗口内部滚动。

如果 PDF.js 因网络原因没有加载成功，网页会自动保留 “View Original PDF” 入口，不影响 PDF 本身访问。

---

## 上传到 GitHub Pages

你的仓库应类似：

```text
guokai-hao.github.io/
├── _config.yml
├── _data/
├── _includes/
├── _layouts/
├── _sass/
├── assets/
├── index.html
├── profile.jpg          # 你的头像，可选
├── CV.pdf               # 你的研究汇报 / PDF
└── ...
```

直接把本 ZIP 解压后的文件上传到 `guokai-hao.github.io` 仓库根目录即可。

> 上传前建议先备份你现有仓库。不要删除你已经上传的 `CV.pdf`。

GitHub Pages 设置继续保持：

- Source: `Deploy from a branch`
- Branch: `main`
- Folder: `/(root)`

---

## 主题来源与许可

本模板基于 [Not Pure Poole](https://github.com/vszhub/not-pure-poole) 修改，保留原项目 MIT License。
