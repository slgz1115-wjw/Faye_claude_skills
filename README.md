# Faye_claude_skills
直接给你可以复制粘贴的内容。在GitHub上找到 `README.md`，点右边的铅笔图标编辑，把现有内容全部替换成下面这段：

````markdown
# Faye_claude_skills

小Faye的Claude Skills 合集，记录用于日常工作的自定义AI工作流。

---

## 目录

| Skill | 功能 |
|-------|------|
| [domain-briefing](./domain-briefing/SKILL.md) | 领域背调 + 录音稿知识提炼 → 输出完整调研文档 |

---

## 如何使用这些Skill

在 Claude.ai 的 Settings → Skills 中，上传对应的 `.skill` 文件即可启用。

---

## 如何更新/新增Skill到这个Repo

### 环境准备（只需做一次）

1. 确保本地已安装 Git
2. 克隆repo到本地：
   ```bash
   git clone https://github.com/slgz1115-wjw/Faye_claude_skills.git
   cd Faye_claude_skills
   ```
3. GitHub认证：用Personal Access Token代替密码
   - GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
   - Generate new token，勾选 `repo` 权限，复制Token备用
   - push时Username填 `slgz1115-wjw`，Password填Token

### 新增Skill

1. 把新的 `.skill` 文件改后缀为 `.zip` 并解压，得到 `skill名/` 文件夹
2. 将文件夹拖入本地的 `Faye_claude_skills/` 目录
3. 在终端执行：
   ```bash
   cd Faye_claude_skills
   git add .
   git commit -m "Add [skill名] skill"
   git push
   ```

### 修改已有Skill

1. 直接在本地编辑对应的文件
2. 在终端执行：
   ```bash
   git add .
   git commit -m "Update [skill名]: [改了什么]"
   git push
   ```

### 常见问题

**push时提示代理错误（port 7897）**
```bash
git config --global --unset http.proxy
git config --global --unset https.proxy
```
然后重新push。

**push时提示authentication failed**
密码框里填Personal Access Token，不是GitHub登录密码。

---

## 注意事项

- Mac系统会自动生成 `.DS_Store` 文件，已在 `.gitignore` 中屏蔽，无需处理
- 直接在 `main` 分支上操作即可，不需要建branch
````

编辑完拉到底部，点 **Commit changes** 保存。
