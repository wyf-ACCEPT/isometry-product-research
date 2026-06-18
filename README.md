# Isometry · Agentic Payment 产品方向研究

Tabula / Isometry 团队针对 **agentic payment（AI agent 自己付钱）** 产品方向的研究产物。

每个人 owns 一个论点 / 一个赌注，产出是**被论证过的立场**，而不是一张竞品对比地图。三块研究各自做成一个**单文件 HTML 页面**，统一沿用同一套视觉语言（暖纸色 + neo-brutalist 硬阴影 + 桔色主调，双语）。

## 目录

```
site/
├── pland-stripe.html            PlanD  —— Stripe 母题拆解：三块脏活 + 探索历程
├── sipeng-permit.html           思芃    —— Spend Permit：agentic payment 产品概念
└── yingmiao-no-stablecoin.html  应淼    —— 立论：agentic payment 的赢家不需要稳定币
```

| 页面 | 负责人 | 标题 / 主题 |
|---|---|---|
| `site/pland-stripe.html` | **PlanD** | Stripe 的三块脏活｜Stripe 母题拆解（防欺诈 / 小商家托管 / 灵活接入 + 产品一号位探索历程） |
| `site/sipeng-permit.html` | **思芃** | Isometry｜Agentic Payment 方向评审（Spend Permit：给 agent 一张消费许可证） |
| `site/yingmiao-no-stablecoin.html` | **应淼** | 立论｜Agentic Payment 的赢家不需要稳定币（反方论证） |

## 如何查看

每个页面都是自包含的单文件 HTML（CSS / JS 全部内联），**无需 build、无依赖**：

- 本地直接用浏览器打开 `site/<页面>.html` 即可。
- 含交互的页面（选择题、阶梯、selector 等）在普通浏览器里都能正常运行。

## 协作约定

每个人**只改自己名下的页面**（以自己名字开头的那个），不动别人的 HTML。详见 [`CLAUDE.md`](./CLAUDE.md)。
