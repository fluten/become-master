# 🚀 直接成为.skill

> 想成为某领域大师？直接成为。

一个 Claude Skill，帮你在 5 分钟内获得某个领域的「大师速成包」，让你能跟该领域的从业者侃侃而谈，不露怯。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE) [![Claude Skill](https://img.shields.io/badge/Claude-Skill-blueviolet?logo=anthropic)](https://claude.ai) [![GitHub](https://img.shields.io/badge/GitHub-fluten-181717?logo=github)](https://github.com/fluten) [![中文](https://img.shields.io/badge/语言-中文-red)](.)
## 它能做什么？

告诉 Claude 你想成为哪个领域的行家——咖啡、红酒、机械表、私募基金、养狗、当代艺术、摄影……任何领域都行。

它会输出一整套**社交作战手册**：

| 模块 | 作用 |
|------|------|
| 🎯 身份定位 | 一句话定义你是谁 |
| 🗣️ 行话黑话 | 入场券，8-12 个核心术语 + 自然话术 |
| 🔥 装备/品牌鄙视链 | 大众品牌→顶级→**懂哥之选**（小众圈内封神款） |
| 🧠 核心认知 | 行家 vs 外行认知差最大的几个点 |
| 💣 谈资弹药 | 可以主动抛出的话题和故事 |
| 📊 段位鉴别 | 快速判断对方是什么水平 |
| ⚠️ 避坑指南 | 最容易暴露外行的常见错误 |
| 🏆 装逼终极技 | 让对方刮目相看的冷门狠货 |
| 🪂 救场话术 | 答不上来时的万能逃生方案 |
| 📊 脑图速记卡 | 一张 mermaid 脑图，4 层价值优先级取舍，出门前 30 秒看一眼 |

## 亮点

- **实战导向，不是百科全书**：每个知识点都能直接用在真实对话里
- **品牌鄙视链 + 懂哥之选**：具体的品牌、产品、价位、口碑——只有花过钱踩过坑的人才知道的东西
- **救场话术**：6 种话术应对 + 物理逃离终极方案（出去不是上厕所，是偷偷查资料），永远不会当场翻车
- **脑图速记卡**：mermaid mindmap + ASCII 树双份输出，按「最高频/最高 ROI/底线/边缘」4 层强制取舍，18 个节点装下整个领域的精华
- **有态度、有立场**：像老行家在教兄弟，不是两边讨好的废话

## 安装

### 方式一：Claude 桌面端 / Claude.ai

下载 `become-master.skill` 文件，在 Claude 桌面端或 Claude.ai 中导入即可。

### 方式二：Claude Code

Claude Code 直接读 `~/.claude/skills/` 或项目级 `.claude/skills/` 下的 SKILL.md，把整个 `become-master/` 目录拷过去就能用。

**全局安装**（所有项目都可用，推荐）：

```bash
# macOS / Linux
mkdir -p ~/.claude/skills
cp -r become-master ~/.claude/skills/

# Windows (PowerShell)
New-Item -ItemType Directory -Force "$HOME\.claude\skills" | Out-Null
Copy-Item -Recurse become-master "$HOME\.claude\skills\"
```

**项目级安装**（只在当前 repo 生效，适合团队共享）：

```bash
mkdir -p .claude/skills
cp -r become-master .claude/skills/
```

装完之后，在 Claude Code 里直接说「我想直接成为 XXX」就会自动触发，不需要手动 `/skill` 调用。

### 方式三：OpenClaw（小龙虾 🦞）

OpenClaw 的 skill 格式跟 Claude Code 完全一致，安装路径也是 `.claude/skills/`，用上面 Claude Code 同样的命令拷贝即可——同一份 SKILL.md，两边通用，不需要重写。

### 验证安装

随便挑一个领域试试：

```
我想直接成为精品咖啡大师
```

Claude 应该立刻进入「老行家教兄弟」的模式，输出整套作战手册。如果它没有触发，检查一下：
- SKILL.md 是否在正确路径下（`<skills 目录>/become-master/SKILL.md`，而不是直接放散件）
- frontmatter 的 `name` 和 `description` 字段是否完整

## 使用示例

```
我想直接成为精品咖啡大师
```
```
教我成为私募基金行家，下周要跟投资人吃饭
```
```
我要直接成为机械表玩家，不想在表友群里露怯
```
```
帮我速成红酒知识，今晚有个酒会
```

## 文件结构

```
become-master/                  # 仓库根目录
├── README.md                   # 你正在看的这个
├── LICENSE                     # MIT 协议
├── become-master.skill         # 打包好的 skill 文件，用于 Claude.ai / 桌面端导入
└── become-master/              # skill 源目录，拷到 .claude/skills/ 即可被 Claude Code / OpenClaw 加载
    └── SKILL.md                # 技能定义文件（frontmatter + 正文）
```
