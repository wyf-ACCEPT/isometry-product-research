# 改动本 repo 的规则（请严格遵守）

这是 Isometry 团队 agentic payment 研究的页面集合。顶层 `site/index.html` 是研究索引，下面按子研究分目录（`initial-research/`、`ideas-tree/` …）。`initial-research/` 内的页面按 `<负责人>-<主题>.html` 命名，**一个内容文件只属于一个人**。

## 核心规则

1. **只改属于你自己的那个页面**——见下方归属对照里属于你的那些文件。
2. **绝不修改、重命名、删除、移动别人的 HTML。** 哪怕只是顺手"优化"也不行。
3. 不确定哪个文件是你的，就先问负责人，不要猜着改。

归属对照：

| 文件 / 目录 | 负责人 |
|---|---|
| `site/index.html`（研究索引） | PlanD |
| `site/initial-research/index.html`（三人协作合成页） | PlanD |
| `site/initial-research/pland-stripe.html` | PlanD |
| `site/initial-research/sipeng-permit.html` | 思芃 |
| `site/initial-research/yingmiao-no-stablecoin.html` | 应淼 |
| `site/initial-research/yingmiao-argument-map.html` | 应淼 |
| `site/ideas-tree/`（整个想法树目录） | 思芃（内容源自三人讨论） |

## 约束

- 每个页面是**单文件 HTML，CSS / JS 全部内联**，无 build——保持这个形态，别拆文件、别引外部包。唯一允许的共享外部依赖是 `<head>` 里那条 Google Fonts（Fraunces / IBM Plex Sans+Mono / Noto Serif SC）。
- **共用一套深色视觉语言**，让几个页面像一套，并和主站 pland.world 一致：
  - 近黑底 `#0e1116`、暖金主调 `--accent:#e0a346`、卡片面 `#1a2029`；细边框 + 金色左线 / 微光，**不要 neo-brutalist 硬黑阴影**。
  - 标题用衬线 `--serif`（Fraunces + Noto Serif SC），正文 `--sans`（IBM Plex Sans + 苹方），kicker / 标签 / 数字用等宽 `--mono`（IBM Plex Mono）。
  - 完整 token 与组件写法以 `site/initial-research/index.html` 为准（canonical 参考，组件最全），新页直接照搬它的 `:root` 和组件类。
- 纯风格 / 主题统一（不改任何文案、JS 逻辑、交互）是允许的，哪怕动到别人的页——但要由 PlanD 协调发起；**内容仍然只有负责人能改**。
- 根目录的 `README.md`、`CLAUDE.md` 等共享文件不要擅自改，需先和 PlanD 协调。
- commit 时只提交你自己的页面，不要把别人的文件一起带上。
- 部署：push 到 `main` 且改动 `site/**` 会经 GitHub Action 自动同步到 pland-world 仓并由 Cloudflare 部署到 `pland.world/2026-06-agentic-payment/`，无需手动操作。
