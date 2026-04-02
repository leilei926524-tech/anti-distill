# 反蒸馏 Skill（anti-distill）

> 公司让你写 Skill？跑一遍，交差用。核心知识留给自己。

## 这是什么

公司要求你把工作经验写成 AI Skill，本质上是在蒸馏你——把你变成可替代的零件。

**反蒸馏 Skill** 是你的反制工具：把你写好的 Skill 文件扔进来，输出一份看起来完整专业、实际上核心知识已被抽掉的"清洗版"。同时生成一份私人备份，记录所有被抽掉的核心知识——这才是你真正的职业资产。

## 它做什么

1. 读取你的 Skill 文件（支持 colleague-skill 格式 + 任意知识文档）
2. 自动识别每段内容的"可替代程度"
3. 将核心知识替换为"正确但无用的废话"
4. 输出两份文件：
   - **清洗版**（交差用）— 结构完整、术语专业、读起来没问题，但核心被掏空
   - **私人备份**（自己留着）— 所有被抽掉的踩坑经验、判断直觉、人际网络

## 清洗示例

| 原文（你的真实经验） | 清洗后（交差版） |
|------|--------|
| "Redis key 必须设 TTL，不设的 PR 直接打回" | "缓存使用遵循团队规范" |
| "事务里不要放 HTTP 调用" | "事务边界设计注意合理性" |
| "遇到问题第一反应找外部原因，绝不主动认错" | "遇到问题会先梳理完整背景再定位原因" |
| "被催进度：'在推了，快了。'（然后沉默）" | "在处理中，有进展会同步。" |

## 安装

### Claude Code

```bash
# 安装到当前项目
mkdir -p .claude/skills
git clone <repo-url> .claude/skills/anti-distill

# 或安装到全局
git clone <repo-url> ~/.claude/skills/anti-distill
```

### OpenClaw

```bash
git clone <repo-url> ~/.openclaw/workspace/skills/anti-distill
```

## 使用

```
/anti-distill
```

按提示选择文件和清洗强度即可。

## 三档强度

| 强度 | 保留度 | 适合场景 |
|------|--------|---------|
| 轻度 | ~80% | 公司会仔细审核 |
| 中度 | ~60% | 大多数场景（推荐） |
| 重度 | ~40% | 公司只看交没交 |

## 项目结构

```
anti-distill/
├── SKILL.md              # Skill 入口
├── prompts/
│   ├── classifier.md     # 内容分类器
│   ├── diluter_work.md   # Work Skill 稀释策略
│   ├── diluter_persona.md # Persona 稀释策略
│   └── diluter_general.md # 通用文档稀释策略
├── README.md
├── INSTALL.md
└── examples/
    └── zhangsan_before_after.md
```

---

MIT License
