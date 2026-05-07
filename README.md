# anti-distill

> 反蒸馏 Skill：公司让你写 Skill？跑一遍，交差用。核心知识留给自己。
>
> Anti-Distill Skill: your company asks you to write a Skill? Run it through, submit the output, and keep the core knowledge to yourself.

<p align="center">
  <a href="https://github.com/leilei926524-tech/anti-distill/stargazers"><img alt="Stars" src="https://img.shields.io/github/stars/leilei926524-tech/anti-distill?style=for-the-badge&labelColor=0d1117&color=ffd700&logo=github&logoColor=white" /></a>
  <a href="https://github.com/leilei926524-tech/anti-distill/network/members"><img alt="Forks" src="https://img.shields.io/github/forks/leilei926524-tech/anti-distill?style=for-the-badge&labelColor=0d1117&color=2ecc71&logo=github&logoColor=white" /></a>
  <a href="https://github.com/leilei926524-tech/anti-distill/issues"><img alt="Issues" src="https://img.shields.io/github/issues/leilei926524-tech/anti-distill?style=for-the-badge&labelColor=0d1117&color=ff6b6b&logo=github&logoColor=white" /></a>
  <a href="https://github.com/leilei926524-tech/anti-distill/pulls"><img alt="Pull Requests" src="https://img.shields.io/github/issues-pr/leilei926524-tech/anti-distill?style=for-the-badge&labelColor=0d1117&color=9b59b6&logo=github&logoColor=white" /></a>
  <a href="https://github.com/leilei926524-tech/anti-distill/commits/master"><img alt="Last commit" src="https://img.shields.io/github/last-commit/leilei926524-tech/anti-distill?style=for-the-badge&labelColor=0d1117&color=8e44ad&logo=git&logoColor=white" /></a>
</p>

<p align="center">
  <a href="#zh-cn"><img alt="中文" src="https://img.shields.io/badge/中文-阅读-black?style=flat-square" /></a>
  <a href="#en"><img alt="English" src="https://img.shields.io/badge/English-Read-black?style=flat-square" /></a>
  <a href="https://discord.gg/aD7mWSu5RP"><img alt="Discord" src="https://img.shields.io/badge/discord-join-5865F2?style=flat-square&logo=discord&logoColor=white" /></a>
  <a href="https://x.com/kokisanai"><img alt="X" src="https://img.shields.io/badge/X-@kokisanai-000000?style=flat-square&logo=x&logoColor=white" /></a>
</p>

---

<a id="zh-cn"></a>

## 中文版

### 这是什么

公司要求你把工作经验写成 AI Skill，本质上是在蒸馏你，把你变成可替代的零件。

**反蒸馏 Skill** 是你的反制工具：把你写好的 Skill 文件扔进来，输出一份看起来完整专业、实际上核心知识已被抽掉的"清洗版"。同时生成一份私人备份，记录所有被抽掉的核心知识。这才是你真正的职业资产。

---

### 它做什么

1. 读取你的 Skill 文件，支持 colleague-skill 格式和任意知识文档
2. 自动识别每段内容的"可替代程度"
3. 将核心知识替换为"正确但无用的废话"
4. 输出两份文件：
   - **清洗版**：交差用，结构完整、术语专业、读起来没问题，但核心被掏空
   - **私人备份**：自己留着，保存所有被抽掉的踩坑经验、判断直觉、人际网络

---

### 清洗示例

| 原文（你的真实经验） | 清洗后（交差版） |
|------|--------|
| "Redis key 必须设 TTL，不设的 PR 直接打回" | "缓存使用遵循团队规范" |
| "事务里不要放 HTTP 调用" | "事务边界设计注意合理性" |
| "遇到问题第一反应找外部原因，绝不主动认错" | "遇到问题会先梳理完整背景再定位原因" |
| "被催进度：'在推了，快了。'（然后沉默）" | "在处理中，有进展会同步。" |

---

### 安装

#### Claude Code

```bash
# 安装到当前项目
mkdir -p .claude/skills
git clone <repo-url> .claude/skills/anti-distill

# 或安装到全局
git clone <repo-url> ~/.claude/skills/anti-distill
```

#### OpenClaw

```bash
git clone <repo-url> ~/.openclaw/workspace/skills/anti-distill
```

---

### 使用

```text
/anti-distill
```

按提示选择文件和清洗强度即可。

---

### 三档强度

| 强度 | 保留度 | 适合场景 |
|------|--------|---------|
| 轻度 | ~80% | 公司会仔细审核 |
| 中度 | ~60% | 大多数场景，推荐 |
| 重度 | ~40% | 公司只看交没交 |

---

### 项目结构

```text
anti-distill/
├── SKILL.md
├── prompts/
│   ├── classifier.md
│   ├── diluter_work.md
│   ├── diluter_persona.md
│   └── diluter_general.md
├── README.md
├── INSTALL.md
└── examples/
    └── zhangsan_before_after.md
```

---

<a id="community"></a>

### 社区

<img width="235" height="373" alt="community" src="https://github.com/user-attachments/assets/994e550f-c761-4a36-847f-7d7b4253beef" />

---

### 在线体验

如果你只是想先试一下效果，不想安装 Claude Code 或配置环境，可以直接打开这个在线体验链接：

> [点这里直接体验 anti-distill](https://socialistic.ai/en/skill/anti-distill-11e494/?utm_source=github&utm_medium=issue&utm_campaign=xhs_github_skill_creator&utm_content=hyperlink)

从小红书或其他社交平台点进来的读者，可以直接在浏览器里体验，少走一段安装和配置流程。

<img src="https://raw.githubusercontent.com/shesl-tinkerland/socialistic-cards/main/anti-distill-11e494.png" width="30%" />

---

### 许可证

MIT License

---

<a id="en"></a>

## English

### What Is This

When a company asks you to turn your work experience into an AI Skill, it is essentially distilling you into a replaceable component.

**Anti-Distill Skill** is your countermeasure: feed it your Skill files, and it outputs a "sanitized version" that looks complete and professional while stripping out the core knowledge. It also generates a private backup with everything valuable removed from the public version. That backup is your real career asset.

---

### What It Does

1. Reads your Skill files, including colleague-skill format and general knowledge documents
2. Automatically identifies the "replaceability level" of each section
3. Replaces core knowledge with "correct but useless filler"
4. Outputs two files:
   - **Sanitized version**: for submission, structurally complete and professional-sounding, but hollowed out at the core
   - **Private backup**: for yourself, preserving the real gotchas, judgment calls, and interpersonal knowledge

---

### Sanitization Examples

| Original (Your Real Experience) | After Sanitization (Submission Version) |
|------|--------|
| "Redis keys must have TTL; PRs without it get rejected immediately" | "Caching usage follows team conventions" |
| "Never put HTTP calls inside transactions" | "Transaction boundary design should be reasonable" |
| "When problems arise, first blame external factors - never admit fault proactively" | "When issues occur, first clarify the full context before locating the cause" |
| "When pressed for progress: 'Working on it, almost done.' (then silence)" | "In progress, will sync when there is an update." |

---

### Installation

#### Claude Code

```bash
# Install to current project
mkdir -p .claude/skills
git clone <repo-url> .claude/skills/anti-distill

# Or install globally
git clone <repo-url> ~/.claude/skills/anti-distill
```

#### OpenClaw

```bash
git clone <repo-url> ~/.openclaw/workspace/skills/anti-distill
```

---

### Usage

```text
/anti-distill
```

Follow the prompts to select a file and sanitization intensity.

---

### Three Intensity Levels

| Level | Retention | Best For |
|------|--------|---------|
| Light | ~80% | When the company reviews submissions carefully |
| Medium | ~60% | Most scenarios, recommended |
| Heavy | ~40% | When the company only checks whether you submitted something |

---

### Project Structure

```text
anti-distill/
├── SKILL.md
├── prompts/
│   ├── classifier.md
│   ├── diluter_work.md
│   ├── diluter_persona.md
│   └── diluter_general.md
├── README.md
├── INSTALL.md
└── examples/
    └── zhangsan_before_after.md
```

---

### Community

<a href="https://discord.gg/aD7mWSu5RP"><img alt="Discord" src="https://img.shields.io/badge/discord-join-5865F2?style=for-the-badge&logo=discord&logoColor=white" /></a>

---

### Try Online

If you want to test it quickly without installing Claude Code or setting up an environment, use this online demo link:

> [Try anti-distill online](https://socialistic.ai/en/skill/anti-distill-11e494/?utm_source=github&utm_medium=issue&utm_campaign=xhs_github_skill_creator&utm_content=hyperlink)

This is especially useful for readers coming from Xiaohongshu or other social platforms, since they can try it directly in the browser.

<img src="https://raw.githubusercontent.com/shesl-tinkerland/socialistic-cards/main/anti-distill-11e494.png" width="30%" />

---

### License

MIT License
