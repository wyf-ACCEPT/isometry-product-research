# 三人产品形态讨论 · 会议要点（2026-06-19）

> 参会：PlanD（我）、谢思芃（Sipeng）、应淼（YingMiao）。时长约 55 分钟。
> 原始转录见 `context/6f19-Isometry-Product-产品形态讨论.txt`。
> 本文是给"群内 present 前"的内部复盘：判断 + 新点 + 待补的洞。

---

## 一、整体判断：能不能顺利在群里 present？

**骨架很强，但现在还不是"能直接 present"的状态——缺一次合成 + 思芃那部分要重写。**

最大的亮点：**三个人从三个完全不同的入口出发，最后都收敛到同一个点——「授权与责任 / 赔付（underwriting）」**。

- 我：从 Stripe 三块脏活 → 防欺诈最可迁移
- 思芃：从 anyway.sh 拆解 → 责任层
- 应淼：从"赢家要不要稳定币"反证 → 核心是授权与责任，不是新轨道

这个"殊途同归"本身就是最有说服力的 presentation 主线——比任何单点都强，因为它是三个独立赌注撞到一起。这正是 Herbie 要的 product insight，不是 GTM。

但有三件事让它现在 present 会卡：

1. **还没合成**。现在是三份独立的 deck，我们自己也说了"几个的应该都要合并起来才能好说"。群里 present 必须是一条线，不是三个人轮流讲 20 分钟。
2. **思芃自己承认他那部分没 refine**：术语多、大白话没写进 HTML、讲得不流畅，要重写。这是他自己点名的，present 前必须等他更新。
3. **最关键的问题没答案**：Isometry 到底**能不能真的赔付 / 兜底**？思芃把它当 open question 抛出来了（"我们有没有能力做这个赔付"），还提到赔付可能要打官司、要托管能力。这是整个 thesis 的命门——如果答不上，"责任层"就有掉回 anyway.sh 那种"更聪明的管子"的风险。

---

## 二、这次讨论里冒出来的新点（kickoff / handoff 里没有的）

按"新增量"排，我认为有价值的有这几个：

1. **三方收敛到"授权与责任"**（meta-finding）——这是最大的新增，直接抬升了信念度。

2. **应淼：「可逆性是 feature，不是 bug」** —— 很锋利的新框架。稳定币 A→B 不可逆，要退款得发一笔全新的 B→A 交易 + 一套系统去控制；而 agent 会幻觉、一定会出错，所以"可逆"恰恰是 agent 支付的刚需。这一条直接把稳定币的"特性"翻成"缺陷"。

3. **应淼：tokenization 正在吃掉稳定币的微支付优势** —— 带证据的新论据。Visa/MC 已经在给 agent 发限额 token（充 \$200、按天统一结算），长尾小费被批量结算消解；x402 / Coinbase 原生稳定币只能做 M2M，买洗衣机 / 淘宝那种消费场景做不了。结论金句：**"稳定币主要还是在我们自己小圈子里自嗨"**。

4. **应淼的两类场景 + 三个问题** —— 干净的分析框架：
   - 场景①：用户把采购外包给 agent；场景②：agent ↔ agent（M2M）互相调用服务 / API。
   - 三问：(a) 是不是我授权的（有没有被盗刷）？(b) 金额对不对 / 能不能叫停（防失控消费）？(c) 出错能不能追责赔付？
   - 这套可以直接当 present 的提纲。

5. **思芃：意图—结算之间的 gap，Isometry 当那道"阀门 / gate"** + 谓词化 / 电路化 / ZK + **用 TOS / 用户协议当"承保契约"**（哪些事我们签字保证成功）。方向新，但最虚，见第三节。

6. **思芃：Canton / Tempo 竞品拆解** —— 他们做的是金融层合规（链上链下搬钱、政府合作、隐私、证明），**没做"agent 花错钱谁负责"这层支付责任**。这是"别人没做的空地"的具体证据。（注：转录里的 "Temple" 是 Tempo 的误转。Tempo 调研已完成，结论见文末「附」——**确认不原生支持退款 / 不做链上担责**，反而强力坐实了我们的 thesis。）

7. **FX × agentic payment 的结合点**（思芃）—— Isometry 本来做 FX，非洲 / 南美用户用 agent 自动换币换法币，正好骑 Lindsay（小雨）的银行 connection。这是对"为什么是我们能做"的具体回答，把研究勾回了 Isometry 的真实资产。

8. **pivot 风险被点名** —— Isometry 本来做链，"责任层"是个大 pivot，柯总 / Herbie 接不接受、感不感兴趣，是个战略问题，present 时要主动 acknowledge，别假装不存在。

9. **思芃的 rail-agnostic 重构**："Isometry 后面是不是稳定币、还是走真实金融体系，从产品层面都无所谓，只要能用"——这条正好和应淼的结论咬合，可以当统一口径。

---

## 三、present 前必须补的洞

- **回答"能不能赔付"**：哪怕给个分层答案——哪些风险我们签 TOS 兜（可谓词化、可模板化的）、哪些我们不碰、快速赔付通道走什么机制。不答这个，责任层立不住。
- **处理一个内在张力**：这条线母体是 Isometry FX / **稳定币**基建，而应淼的结论是"稳定币非必须"。群里一定有人觉得"你们自己研究把自己产品否了"。要用应淼的"这是被指派的对抗式赌注" + 思芃的"rail-agnostic 产品优先"来正面框住，变成"我们对稳定币的信念是被压力测试过的"，而不是打脸。
- **几个事实点 present 前 tighten 一下**：Visa/MC 的 agent token 细节、~~Tempo 是否原生支持退款~~（已查实：不支持，见文末附）、x402 only-M2M、责任上限（港 500 / 英镑 100）——大方向对，但面对挑剔听众要能顶住追问。

---

## 四、后续 TODO（本次会后定的）

1. ~~总结会议要点~~（本文）。
2. 改网页：(a) 思芃先 refine 他那页 → (b) 主页 `index.html` 做"串起来 / 合成" → (c) 最后统一改风格。
3. ~~调研 Tempo 是否支持退款~~（已完成，见文末附）。
4. 群内发言：先发网页 → 再发几段研究背景 / 结论 / 出发点（分条微信消息）→ 配部署好的网页一起发群。

---

## 附：Tempo 退款调研结论（2026-06-19）

> 转录里的 "Temple / temple" 是 **Tempo** 的误转。来源以 Tempo 官方文档、Paradigm / Stripe 博客、CoinDesk / The Block 为准（链接见末）。

**Tempo 是什么**：Stripe + Paradigm 共同孵化的"支付优先"EVM-兼容 L1，Paradigm 联创 Matt Huang 牵头。2025-09-04 宣布，**2026-03-18 主网上线**。约 0.6s 终局、目标 10w+ TPS、gas 用 USDC/USDT 付。主网随 **MPP（Machine Payments Protocol，与 Stripe 共建）** 一起发，专做 agent↔agent（M2M）随 HTTP 请求内联的自治支付（无需逐笔人工签字）。设计期有 Anthropic、Visa、OpenAI、Deutsche Bank、Shopify、Nubank 等参与。

**核心问题——是否原生支持退款？→ 不支持（协议层）。**

- 协议层**没有** chargeback / clawback / 争议 / 撤销 机制。一笔 A→B 结算完，退款只能由 B 发一笔全新的 B→A，或走 Stripe 的链下流程。
- **关键陷阱**：Tempo 流式支付（streamed payment）文档里有 "refund unused deposit"，但那只是**退还托管池里没花掉的预存款**（事前预授权池），**不是把已结算的钱撤回**——别被这个词误导，present 顶追问时要点破这点。
- Tempo 内置风控全是**事前预防型**：每个 access key 的限额 / 过期 / 调用范围 + 托管计量。**对"agent 花错钱 / 幻觉后谁负责"完全不做链上担责**，明确甩给链下协议。
- 唯一沾"退款"的高层能力来自 **Stripe 链下结算层**（Stripe MPP 博客称同一套基础设施可给 agent 做 refund），这是 Stripe 商户侧产品功能，**不是 Tempo 链的原生可逆原语**。

**对我们 thesis 的意义（全是利好）：**

1. **应淼说对了**——"Tempo 不原生支持退款"已证实。
2. **直接坐实"可逆性是 feature 不是 bug"**：连 Stripe 亲自下场、专为 agent 设计的 Tempo 都不解决可逆。
3. **坐实"责任层是空地"**：连 Tempo 都把"agent 花错钱谁负责"留给链下——正是我们要填的坑。
4. **彩蛋**：Tempo 背后是 **Stripe**，正好咬合 PlanD 的 Stripe 母题（Stripe 既是"收钱时代"的赢家，又在下注"agent 付钱时代"的新链）。

**来源**：
- Paradigm 公告 https://www.paradigm.xyz/2025/09/tempo-payments-first-blockchain
- Tempo 官网 https://tempo.xyz/ ；机器支付文档 https://docs.tempo.xyz/guide/machine-payments
- 流式（托管）支付 https://docs.tempo.xyz/guide/machine-payments/streamed-payments
- Stripe MPP 博客 https://stripe.com/blog/machine-payments-protocol
- CoinDesk（主网上线 2026-03-18）https://www.coindesk.com/tech/2026/03/18/stripe-led-payments-blockchain-tempo-goes-live-with-protocol-for-ai-agents
- The Block https://www.theblock.co/post/394131/tempo-mainnet-goes-live-with-machine-payments-protocol-for-agents
