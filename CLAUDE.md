# 改动本 repo 的规则（请严格遵守）

这是 Isometry 团队 agentic payment 研究的页面集合。`site/` 下每个 HTML 按 `<负责人>-<主题>.html` 命名，**一个文件只属于一个人**。

## 核心规则

1. **只改属于你自己的那个页面**——即 `site/` 下以你名字开头的 HTML。
2. **绝不修改、重命名、删除、移动别人的 HTML。** 哪怕只是顺手"优化"也不行。
3. 不确定哪个文件是你的，就先问负责人，不要猜着改。

归属对照：

| 文件 | 负责人 |
|---|---|
| `site/pland-stripe.html` | PlanD |
| `site/sipeng-permit.html` | 思芃 |
| `site/yingmiao-no-stablecoin.html` | 应淼 |

## 约束

- 每个页面是**单文件 HTML，CSS / JS 全部内联**，无 build、无外部依赖——保持这个形态，别拆文件、别引外部包。
- 尽量沿用已有的视觉语言（暖纸色背景、neo-brutalist 硬阴影、桔色主调、双语），让几个页面像一套。
- 根目录的 `README.md`、`CLAUDE.md` 等共享文件不要擅自改，需先和 PlanD 协调。
- commit 时只提交你自己的页面，不要把别人的文件一起带上。
