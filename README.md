# Business Council / 商业思维参谋

[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-business--council-blue)](#quick-start)
[![Claude Code Skill](https://img.shields.io/badge/Claude%20Code-Skill-purple)](https://claude.ai/code)
[![License: MIT](https://img.shields.io/badge/License-MIT-black.svg)](LICENSE)

一个同时适用于 **Agent（如 Claude Code、Codex）** 和 **Claude Code 项目级 Skill** 的商业参谋工具：把史蒂夫·乔布斯、埃隆·马斯克、杰夫·贝索斯、黄仁勋四位企业家的公开思维框架，复现在你的真实商业决策里。

An **Agent Skill** and **Claude Code Skill** that channels the thinking of **Steve Jobs, Elon Musk, Jeff Bezos, and Jensen Huang** to help you reason through strategy, product, go-to-market, capital allocation, organization, and crisis decisions.

---

## Why Business Council / 为什么需要商业思维参谋

很多商业问题并不是“没有答案”，而是：

- 创始人被单一视角困住，看不到不同维度上的关键权衡；
- 团队争论的是“谁对谁错”，而不是“在不同权重下各有什么道理”；
- 看了一堆案例，但不知道如何把别人的思维模型迁移到自己的决策里；
- 用 AI 做商业分析时，容易从“启发式推演”滑向“空洞的成功学鸡汤”。

Business Council 的思路是：**不替你拍板，而是让四位顶尖决策者先在你脑子里开一次会。**

```text
你的商业问题
    │
    ▼
┌─────────────────┐
│   模式路由器     │  ← Council / Single / Debate / Add-Mind
└─────────────────┘
    │
    ▼
┌─────────────────────────────────────────────────────────────┐
│                     四位思维模型（MINDS.md）                   │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐    │
│  │  Jobs    │  │  Musk    │  │  Bezos   │  │  Huang   │    │
│  │ 用户体验  │  │ 第一性原理│  │ 客户飞轮  │  │ 零亿美元  │    │
│  │  品味     │  │ 物理极限  │  │ 单向/双向门│  │ 平台生态  │    │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘    │
└─────────────────────────────────────────────────────────────┘
    │
    ▼
┌─────────────────────────────────────────────────────────────┐
│                     输出结构（EXAMPLES.md）                    │
│  问题重述 → 四视角分析 → 综合建议 → 风险提醒                  │
│  （立即行动 / 中期行动 / 长期赌注）                           │
└─────────────────────────────────────────────────────────────┘
```

它不是“成功学生成器”，而是一套逼你把问题从多个维度拆清楚的思维操作系统。

---

## What It Does / 功能

针对一个商业问题，按以下四种模式调用：

| 模式 | 触发词 | 输出 |
|---|---|---|
| **Council 模式** | 直接提问 | 四位企业家分别分析，再给出带权衡的综合建议 |
| **Single Mind 模式** | `@Jobs` / `@Musk` / `@Bezos` / `@Huang` | 只以指定企业家的视角作答 |
| **Debate 模式** | `debate` 或 `辩论` | 四位企业家就同一议题简短辩论，最后给出裁判式结论 |
| **Add-Mind 模式** | `add-mind <人物名>` | 按 `ADD_MIND.md` 框架提取新人物的思维模型卡片 |

所有回答都遵循统一结构：问题重述 → 四视角分析 → 综合建议 → 风险提醒。

---

## What It Will Not Do / 边界

- 不编造四位企业家的具体言论或决策细节；
- 不替代法律、财务、税务、投资等专业咨询；
- 不做“算命式”预测或承诺商业结果；
- 不平均四人意见，综合建议必须基于问题性质做加权权衡；
- Add-Mind 模式不会自动修改你的本地文件，只输出 draft card 和集成说明。

---

## Quick Start / 快速开始

### 1. 让 Agent 帮你安装（推荐）

在 Claude Code、Codex 或其他支持 Skill 的 Agent 里直接说：

```text
帮我安装这个 Skill：https://github.com/GresonKwan/business-council-skill
```

Agent 会判断当前工具的 Skill 目录，并把仓库安装到正确位置。安装完成后，重启 Agent 或新开会话：

```text
/business-council
我刚完成 A 轮，账上有 1500 万美元。董事会建议 50% 做市场、30% 做研发、20% 做储备，我想把 70% 投入研发，帮我分析。
```

### 2. 手动安装到 Claude Code

```bash
cd your-project
mkdir -p .claude/skills
git clone https://github.com/GresonKwan/business-council-skill.git .claude/skills/business-council
```

重启 Claude Code 后即可使用。

### 3. 手动安装到 Codex

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/GresonKwan/business-council-skill.git ~/.codex/skills/business-council
```

### 4. 项目级安装

```bash
cd your-project
git clone https://github.com/GresonKwan/business-council-skill.git .agents/skills/business-council
```

> 不同 Agent 的 Skill 加载路径可能不同。如果让 Agent 自动安装，它会帮你处理这些路径差异。

---

## Usage Examples / 使用示例

### Council 模式：一个产品方向问题

```text
/business-council
我的 SaaS 团队正在争论，是做 AI 客服助手，还是做 AI 销售线索评分工具。
两条路都有市场需求，资源只够做一条。
```

输出会分别从 Jobs（用户体验与品味）、Musk（物理可行性与瓶颈）、Bezos（客户飞轮与长期信任）、Huang（零亿美元市场与平台）四个视角给出判断，并综合成行动清单。

### Single Mind 模式：指定一人

```text
/business-council @Musk 如何降低火箭发射成本？
/business-council @Bezos 这个决策是单向门还是双向门？
```

### Debate 模式：让四人辩论

```text
/business-council debate
我们应该提前 6 个月发布一个还不够完美的产品，还是等到完美再发布？
```

### Add-Mind 模式：扩展参谋团

```text
/business-council add-mind Warren Buffett
/business-council 添加 张一鸣
```

Agent 会先确认人物、询问是否有指定资料，再按 `ADD_MIND.md` 的八个维度输出 draft mind card。

---

## How It Works / 运作机制

### 1. 模式路由（Mode Routing）

`SKILL.md` 顶部的 manifest 告诉 Agent 这是一个 Skill，并定义了四种调用模式：

```text
用户输入
  │
  ├── 无前缀 ────────────────→ Council 模式
  ├── 含 @Jobs / @Musk 等 ───→ Single Mind 模式
  ├── 含 debate / 辩论 ───────→ Debate 模式
  └── 含 add-mind / 添加 ────→ Add-Mind 模式
```

### 2. 思维模型层（Mind Cards）

`MINDS.md` 把每位企业家拆成可复现的维度：

- **核心权重**：用 `X > Y` 表达他做什么决策时最看重什么
- **心智模型**：反复使用的思维框架（如第一性原理、客户飞轮、零亿美元市场）
- **他会问的问题**：模拟其思考起点
- **语言风格**：让输出更接近该人物的表达方式
- **经典案例锚点**：防止把人物扁平化成一个标签
- **使用禁忌**：明确哪些场景不适合套用

### 3. 输出结构层（Examples）

`EXAMPLES.md` 提供统一的输出模板和多个完整示例，确保每次回答都有：

- 问题重述与本质分类
- 四位企业家的核心判断、关键问题、建议
- 综合建议（最优路径 / 关键权衡 / 本周 / 1-3 个月 / 1 年以上）
- 风险提醒与免责声明

### 4. 扩展层（Add-Mind Framework）

`ADD_MIND.md` 是一个标准化的“思维模型提取协议”，让任何人都能把新的企业家/投资人/名人加入参谋团。它要求：

- 多源交叉验证
- 区分事实与推断
- 从八个维度提炼
- 输出可直接集成到 `MINDS.md` 和 `SKILL.md` 的卡片

---

## Repository Structure / 仓库结构

```text
.
├── SKILL.md          # Skill 主配置、模式路由、系统提示
├── MINDS.md          # 四位企业家思维模型卡片
├── ADD_MIND.md       # 新增人物提取框架（8 维度）
├── EXAMPLES.md       # 输出模板与完整示例
├── README.md         # 本文件
├── .gitignore
└── LICENSE           # MIT
```

---

## Adding New Thinkers / 扩展新人物

如果你想把第五位、第六位企业家加入参谋团：

1. 运行 `/business-council add-mind <人物名>`；
2. 按提示提供资料或让 Agent 搜索；
3. 把生成的 draft mind card 追加到 `MINDS.md`；
4. 在 `SKILL.md` 中更新人物列表、`@mention` 规则和复现要点；
5. 可选：在 `EXAMPLES.md` 中补充一个该人物的示例。

详细方法论见 `ADD_MIND.md`。

---

## Disclaimer / 免责声明

本 Skill 仅基于公开、可验证的思维框架做启发式模拟，**不构成**法律、财务、投资、税务或专业战略咨询。涉及高风险决策时，请咨询相应领域的专业人士。

This skill simulates publicly documented thinking frameworks for heuristic purposes only. It does **not** provide legal, financial, investment, tax, or professional strategic advice.

---

## License / 许可证

MIT

欢迎 Fork、扩展和添加你自己的“思维董事会”。
