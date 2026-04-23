# 11. 行业观察、去魅与收束

```mermaid
graph TD
    A["入口 / 分发层"] --> B["应用 / 场景层（含 Agent Runtime）"]
    B --> C["上下文 / 记忆层"]
    B --> D["工具 / 世界连接层"]
    B --> E["Gateway / 模型接入层"]
    E --> F["模型 / 推理层"]
    F --> G["算力 / 基础设施层"]
    C -.-> I["传统互联网 / 既有软件世界"]
    D -.-> I

    classDef neutral fill:#f8fafc,stroke:#cbd5e1,stroke-width:1px,color:#0f172a;
    classDef current fill:#dbeafe,stroke:#2563eb,stroke-width:3px,color:#0f172a;
    classDef overview fill:#eef2ff,stroke:#4f46e5,stroke-width:2px,color:#0f172a;
    class A,B,C,D,E,F,G,I neutral;
    class A,B,C,D,E,F,G overview;
```

讲完入口、应用、工具、记忆、模型、推理和基础设施之后，问题会自然变成另一种形式：这个世界确实很大，但新名词也确实很多，哪些是底层变化，哪些只是包装？这一章处理的正是这个问题。

过去一年里，最容易让业内产生 FOMO 的，通常不是最底层的词，而是最像“一个新控制点正在长出来”的词。按焦虑强度排序，更接近现实的顺序通常是：

1. `skills`  
它最会贩卖接口层焦虑：把“如何指导 agent 操作世界”包装成一个门槛突然下降的新层。尤其在 MCP 刚出来没多久之后再次出现，更容易制造“不用 skills 就会错过一整个能力时代”的感觉。

2. `agent team`  
它会让人误以为“不多 spawn 几个 agent 就已经远远落后于时代”；但现实里真正适合并行的任务并不多，隔离上下文和通信汇总的代价常常会吃掉并行优势，最后主 agent 的上下文几乎一点也没少。

3. `harness engineering`  
它把焦点从“如何定义行为”推向“如何定义目标”，制造一种近似 AGI 的错觉：人类只要说出目标，系统就会自己把过程全部组织出来。

4. `memory`  
它借用了人类记忆这个概念，暗示 agent 一旦接上 memory 就会像真人一样长期连续、准确召回、无限对话；而真实系统里，记忆抽取、去重、更新、过期、冲突和召回噪音依然是具体的工程难题。

5. `MCP`  
相比之下，它带来的焦虑更窄一些，更像标准化和生态兼容焦虑：开发者担心的不是“少了 MCP 就没有智能”，而是“如果未来接口标准逐渐统一，自己会不会被排除在默认生态之外”。

如果再说得直接一点，Anthropic 几乎总是最擅长把一层真实能力重新命名、重新包装，再配上一整套极强传播性的概念叙事；结合 `2026 年 4 月` 围绕 Claude Code 默认推理调整、性能争议、套餐与访问策略变化的公开风波，这种营销姿态只会更让人反感。只是 Claude 在相当长一段时间里确实是 Agent 场景下的优选模型，只能捏着鼻子批判性使用。

这些词之所以会火，并不是没有理由，但真正值得警惕的，不是这些词的热度，而是把某一层能力补丁误认成“底层规律已经彻底改写”。

去魅并不意味着否定热词，而是把它们拆开看。每个热点都可以问三个问题：它到底解决了哪个具体痛点？底层内核是什么？为什么会在这个时间点爆红？有些爆红来自真实技术进步，有些来自产品封装变好了，有些来自命名和传播做得足够强，还有一些来自市场恰好需要一个更容易理解的新标签。

Personal AI 是最好的例子之一。OpenClaw、Hermes、Codex 这一条线，并不是凭空发明了一种全新的底层结构。它真正做的，是把“个人代理可以常驻、可以记住、可以跨入口存在、可以持续和你一起成长”这套体验包装得足够完整、足够诱人，也足够会传播。Hermes 借 memory、self-improving、grows with you 这类叙事继续放大热度，并不是完全换了一个物种，而是在已有 personal agent 形态上把记忆、技能和身份连续性往前推了一层。

Replit 和 Palantir 更适合被放在两种完全不同的位置上看。Replit 更像一个比较干净的正面样本：先是浏览器开发工具和在线协作环境，随后逐步 SaaS 化，长出订阅、团队版、企业版和云上开发底座，最后才在这个已有平台之上叠出 Agent。因此它转向 AI-native 软件生产入口，更像顺着原有资产按部就班往前走，而不是靠新概念制造 FOMO。

Palantir 则更像 FOMO 叙事的反例之一。它的核心产品一直是 `Gotham`、`Foundry`、`Apollo` 和后来的 `AIP`，主要客户是政府、军工、大制造、能源、医药和少数超大企业。它卖的从来不只是软件许可，而是把数据、流程、部署和组织动作深度嵌进客户现场。`Ontology` 最值得批判的地方，是它把并不新鲜的数据建模、对象关系、动作绑定和权限体系，包装成了一个听起来像底层突破的新层。`AIP` 也类似：它不是空气，但更像“让原有平台更容易卖、更容易交付、更容易讲成 AI 故事”，而不是一个已经高渗透、可以单独撑起超高 SaaS 倍数的新软件物种。财务上它当然很强，`FY2025` 收入约 `44.75 亿美元`，但客户总数只有 `954`，前二十名客户的过去十二个月平均收入约 `9390 万美元`；这个结构更像深嵌大客户的高接触式平台公司，而不是靠广泛自助复制长出来的典型 SaaS。更稳的结论是：`Ontology` 更像概念包装，`AIP` 更像真实产品加上被放大的市场叙事。

Palantir 这类案例还有一个更有用的启发：容易引发 FOMO 的概念，往往有几个共同特征。第一，它会把一个真实但复杂的工程问题压缩成一个很短、很大、很像新层的词；第二，它会把局部能力提升讲成系统性范式跃迁；第三，它会让非技术决策者也能一眼看懂“如果不跟进就会错过什么”；第四，它会故意站在一个已经有预算、有人群、也有焦虑的位置上。换句话说，一个概念越容易让人 FOMO，越说明它往往同时命中了真实痛点、传播效率和预算入口。

如果反过来看，一个“容易 FOMO 的概念”通常也是这样被制造出来的：先从一个真实但分散的工程痛点出发，把它重新命名成一个足够大的词；再把这个词放在一个“像新层、像新标准、像新入口”的位置上；接着用少量成功案例证明它并非空气；最后刻意强化时间压力，让团队觉得“现在不做，半年后就会被生态抛下”。这不意味着所有概念都只是包装，而是意味着：越容易激发群体焦虑的词，越应该优先拆回它到底在解决什么底层问题、技术原理到底是什么，以及相对成熟方案它真正优化的方向是什么。真正重要的，是抓住行业方向，而不是急着追逐每一个新名字。

回到学生视角，关键不是立刻给自己套一条职业路线，而是先形成一种参与方式。最值得优先建立的能力，不一定是追逐最前沿模型，而是学会从任务、状态、工具、反馈和系统边界的角度理解 Agent。多理解系统层，而不只盯着模型层；从外部工具接入开始做一些真实的小系统；找一个自己真正理解的场景去落地；保留对新名词的去魅能力。对不是天才的普通计算机学生来说，更高回报的起点往往不是“发明一个更大的模型”，而是学会把模型接进真实系统。

整场分享最后留下来的，不应是一个新名词清单，而应是对标题本身更清楚的回答：**Agent 正在长出的，并不是一个孤立技术点，而是一个由算力、模型、接入层、工具层、记忆层、应用层和入口层共同构成的商业世界。** 这个世界真正有价值的地方，不在于它又多了多少热词，而在于它正在把原本分散的能力、流程、软件入口和商业需求重新组织成新的分工、新的产品形态和新的价值链。

---

## 图片生成 Prompts

先继承这份全局风格控制文档中的所有要求：  
[agent_business_world_slide_image_style.md](/Users/timzhong/msc202604/agent_business_world_slide_image_style.md)

### 图 11.1 FOMO 热点不等于底层规律

在此基础上，为这一部分生成一张横版 slide like image，风格优先做成 **trend deconstruction dashboard**。主题是：**skills、agent team、harness engineering、memory、MCP 是过去一年最容易让业内 FOMO 的几个词**。画面左侧按从上到下的顺序放五张 hot concept cards：skills、agent team、harness engineering、memory、MCP。右侧给每一张卡配一条 very short anxiety label：skills 对应 interface-layer anxiety，agent team 对应 parallelism anxiety，harness engineering 对应 goal-automation anxiety，memory 对应 human-like continuity anxiety，MCP 对应 standardization anxiety。整体像真实市场分析 UI，不要做花哨海报。

### 图 11.2 Personal AI 为什么会爆

在此基础上，为这一部分生成一张横版 slide like image，风格优先做成 **personal agent product timeline UI**。主题是：**OpenClaw, Hermes 这类产品把 personal agent 的体验和叙事推到了更前面**。画面是一条清晰产品演化时间线，带 memory, continuity, always-on, local context 这些关键词。

### 图 11.3 Replit 与 Palantir 的两种 AI 转型

在此基础上，为这一部分生成一张横版 slide like image，风格优先做成 **two-path transformation strategy dashboard**。主题是：**Replit 更像顺着原有入口长出 AI 产品，Palantir 更像真实产品与强叙事同时放大**。左侧是 Replit path，突出 IDE, online runtime, developer workflow, AI-native build入口；右侧是 Palantir path，突出 ontology, AIP, enterprise deployment, services, data platform, market narrative。整体是对照式战略分析图，不要把两边都画成正面样板。

### 图 11.4 新术语、旧技术与商业包装

在此基础上，为这一部分生成一张横版 slide like image，风格优先做成 **concept deconstruction interface**。主题是：**一个容易引发 FOMO 的概念，通常是如何被包装出来的**。画面中央是一张 big concept card，向下拆成四层：real engineering pain point, renamed concept, market narrative, budget / adoption pressure。右侧再加一个 small checklist，写 short signals：sounds like a new layer, easy for CXO to understand, implies time pressure, has a few visible success stories。页面像分析工具。

### 图 11.5 最后收束

在此基础上，为这一部分生成一张横版 slide like image，风格优先做成 **high-end concluding strategy interface**。主题是：**Agent 正在把大模型、软件系统、行业流程和商业需求重新接起来**。画面中央是一条被重新连通的价值链，整体像整场分享的最终收束页，适合叠加结尾大字标题。
