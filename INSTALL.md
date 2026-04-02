# 安装说明

## Claude Code

```bash
# 在 git 仓库根目录执行
cd $(git rev-parse --show-toplevel)

# 方式 1：安装到当前项目
mkdir -p .claude/skills
git clone <repo-url> .claude/skills/anti-distill

# 方式 2：安装到全局
git clone <repo-url> ~/.claude/skills/anti-distill
```

然后在 Claude Code 中说 `/anti-distill` 启动。

## OpenClaw

```bash
git clone <repo-url> ~/.openclaw/workspace/skills/anti-distill
```

## 无需额外依赖

本 Skill 纯文本处理，不需要安装任何 Python 包。
