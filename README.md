# Business Council / 商业思维参谋

[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-business--council-blue)](#quick-start)
[![Claude Code Skill](https://img.shields.io/badge/Claude%20Code-Skill-purple)](https://claude.ai/code)
[![License: MIT](https://img.shields.io/badge/License-MIT-black.svg)](LICENSE)

一个同时适用于 **Agent（如 Claude Code、Codex）** 和 **Claude Code 项目级 Skill** 的商业参谋系统：把史蒂夫·乔布斯、埃隆·马斯克、杰夫·贝索斯、黄仁勋四位企业家的公开思维框架，复现在你的真实商业决策里。

An **Agent Skill** and **Claude Code Skill** that channels the thinking of **Steve Jobs, Elon Musk, Jeff Bezos, and Jensen Huang** to help you reason through strategy, product, go-to-market, capital allocation, organization, and crisis decisions.

---

## Why Business Council / 为什么需要商业思维参谋

很多商业问题并不是“没有答案”，而是：

- 创始人被单一视角困住，看不到不同维度上的关键权衡；
- 团队争论的是“谁对谁错”，而不是“在不同权重下各有什么道理”；
- 看了一堆案例，但不知道如何把别人的思维模型迁移到自己的决策里；
- 用 AI 做商业分析时，容易从“启发式推演”滑向“空洞的成功学鸡汤”。

Business Council 的思路是：**不替你拍板，而是让四位顶尖决策者先在你脑子里开一次会，并且告诉你每个人在什么情境下会犯错。**

```text
你的商业问题
    │
    ▼
┌─────────────────┐
│   模式路由器     │  ← Council / Single / Debate / Add-Mind / Backtest
└─────────────────┘
    │
    ▼
┌─────────────────────────────────────────────────────────────────────────┐
│                         思维模型层                                         │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐ │
│  │  MINDS.md    │  │TIME_SLICES.md│  │ANTI_CASES.md │  │DECISION_LOG.md│ │
│  │              │  │              │  │              │  │              │ │
│  │ canonical    │  │ era variants │  │ boundaries   │  │ backtests    │ │
│  │ mind cards   │  │ @Name:Tag    │  │ anti-patterns│  │ correctability│ │
│  └──────────────┘  └──────────────┘  └──────────────┘  └──────────────┘ │
└─────────────────────────────────────────────────────────────────────────┘
    │
    ▼
┌─────────────────────────────────────────────────────────────┐
│                     输出结构（EXAMPLES.md）                    │
│  问题重述 → 四视角分析（含边界提醒） → 综合建议 → 风险提醒    │
│  （立即行动 / 中期行动 / 长期赌注）                           │
└─────────────────────────────────────────────────────────────┘
```

它不是“成功学生成器”，而是一套逼你把问题从多个维度拆清楚、并知道每个人在哪会犯错的思维操作系统。

---

## What It Does / 功能

针对一个商业问题，按以下五种模式调用：

| 模式 | 触发词 | 输出 |
|---|---|---|
| **Council 模式** | 直接提问 | 四位企业家分别分析，再给出带权衡的综合建议 |
| **Single Mind 模式** | `@Jobs` / `@Musk` / `@Bezos` / `@Huang` | 只以指定企业家的 canonical 视角作答 |
| **Time-Slice 模式** | `@Jobs:Return-1997` / `@Huang:CUDA-2006` 等 | 使用同一人物在特定阶段/情境下的思维变体 |
| **Debate 模式** | `debate` 或“辩论” | 四位企业家就同一问题展开辩论，可指定时间切片变体 |
| **Add-Mind 模式** | `add-mind <人物名>` | 按 `ADD_MIND.md` 框架提取新人物的思维模型卡片 |
| **Backtest 模式** | `backtest` 或“复盘” | 对历史决策或用户决策进行回测，验证思维卡片 |

所有回答都遵循统一结构：问题重述 → 四视角分析（含边界提醒） → 综合建议 → 风险提醒。

---

## What It Will Not Do / 边界

- 不编造四位企业家的具体言论或决策细节；
- 不替代法律、财务、税务、投资等专业咨询；
- 不做“算命式”预测或承诺商业结果；
- 不平均四人意见，综合建议必须基于问题性质做加权权衡；
- Add-Mind 模式不会自动修改你的本地文件，只输出 draft card 和集成说明；
- 明确提示每个模型在什么情境下会失效（参见 `ANTI_CASES.md`）。

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

### Time-Slice 模式：调用特定阶段的人物

```text
/business-council @Jobs:Return-1997 如何拯救产品线臃肿的公司？
/business-council @Huang:CUDA-2006 该不该投资一个没客户的开发者平台？
```

### Debate 模式：让四人辩论

```text
/business-council debate 我们应该提前 6 个月发布一个还不够完美的产品，还是等到完美再发布？
```

也可以让同一人物的不同时间切片互相辩论：

```text
/business-council debate @Musk:SpaceX-2008 vs @Musk:Tesla-2018 钱应该投给谁？
```

### Add-Mind 模式：扩展参谋团

```text
/business-council add-mind Warren Buffett
/business-council 添加 张一鸣
```

Agent 会先确认人物、询问是否有指定资料，再按 `ADD_MIND.md` 的维度（含时间切片、对抗验证、场景测试、边界测试）输出 draft mind card。

### Backtest 模式：历史回测或决策日志

```text
/business-council backtest 如果 2007 年苹果讨论是否取消 iPhone 物理键盘，四位会怎么看？
/business-council 复盘 Amazon Prime 2005
```

---

## How It Works / 运作机制

### 1. 模式路由（Mode Routing）

`SKILL.md` 顶部的 manifest 告诉 Agent 这是一个 Skill，并定义了五种调用模式：

```text
用户输入
  │
  ├── 无前缀 ───────────────────────→ Council 模式
  ├── 含 @Name ─────────────────────→ Single Mind 模式（canonical）
  ├── 含 @Name:Tag ─────────────────→ Time-Slice 模式
  ├── 含 debate / 辩论 ─────────────→ Debate 模式
  ├── 含 add-mind / 添加 ───────────→ Add-Mind 模式
  └── 含 backtest / 复盘 ───────────→ Backtest 模式
```

### 2. 思维模型层（Mind Cards）

`MINDS.md` 把每位企业家拆成可复现的维度：

- **元信息**：人物、阶段、领域、版本、来源
- **核心权重**：用 `X > Y` 表达，并注明适用情境
- **心智模型**：每个模型包含定义、触发条件、执行步骤、边界/反例、高成本坚持点、案例锚点
- **高成本坚持点**：他愿意为哪些选择付出巨大代价
- **使用禁忌**：具体而不是泛泛

### 3. 时间切片层（Time Slices）

`TIME_SLICES.md` 让同一人物在不同时代/情境下有不同的权重和风格。例如：

- `@Jobs:Return-1997`：生存 > 完美，适合 turnaround
- `@Jobs:iPhone-2007`：整体体验 > 市场份额，适合定义新品类
- `@Musk:SpaceX-2008`：生存 > 使命，适合创业生死线
- `@Musk:Tesla-2018`：瓶颈优先 > 宏大叙事，适合产能危机

### 4. 反例层（Anti-Cases）

`ANTI_CASES.md` 为每个心智模型提供边界：什么场景适合、什么场景会失效、为什么、用什么替代。确保 skill 不会把一个人误用到他不擅长的领域。

### 5. 决策日志层（Decision Log）

`DECISION_LOG.md` 用历史回测验证思维卡片的可修正性。每个回测都包含：背景、问题、各视角预测、实际选择、结果、可修正性记录。

### 6. 扩展层（Add-Mind Framework）

`ADD_MIND.md` 是一个标准化的“思维模型提取协议”，包含：

- 收集资料
- 时间切片
- 提取维度
- 对抗验证
- 场景测试
- 边界测试
- 生成卡片
- 集成入 skill
- 迭代归档

---

## Repository Structure / 仓库结构

```text
.
├── SKILL.md                         # Skill 主配置、模式路由、系统提示
├── MINDS.md                         # 四位企业家 canonical 思维模型卡片
├── TIME_SLICES.md                   # 时间切片变体（@Name:Tag）
├── ANTI_CASES.md                    # 每个心智模型的边界与反例
├── DECISION_LOG.md                  # 历史回测与决策追溯模板
├── ADD_MIND.md                      # 新增人物提取框架（含对抗验证、场景测试）
├── EXAMPLES.md                      # 输出模板与完整示例
├── TEMPLATES/
│   ├── mind-card-template.md        # 标准思维卡片模板
│   └── decision-trace-template.md   # 标准决策追溯模板
├── README.md                        # 本文件
├── LICENSE                          # MIT
└── .gitignore
```

---

## Adding New Thinkers / 扩展新人物

如果你想把第五位、第六位企业家加入参谋团：

1. 运行 `/business-council add-mind <人物名>`；
2. 按提示提供资料或让 Agent 搜索；
3. 把生成的 draft mind card 追加到 `MINDS.md`；
4. 在 `TIME_SLICES.md` 中添加 1–2 个时间切片变体；
5. 在 `ANTI_CASES.md` 中添加每个心智模型的反例；
6. 在 `DECISION_LOG.md` 中添加至少一个历史回测案例；
7. 在 `SKILL.md` 中更新人物列表、`@mention` 规则和时间切片标签；
8. 可选：在 `EXAMPLES.md` 中补充一个使用该人物的示例。

详细方法论见 `ADD_MIND.md`，标准格式见 `TEMPLATES/mind-card-template.md`。

---

## Success Criteria / 如何判断这个 Skill 有效

1. **可复现性**：拿到卡片的人，能在陌生问题上复现他的思考。
2. **可区分性**：四个人同时回答一个问题，输出能明显看出是谁；同一人物的不同时间切片也能区分。
3. **可纠错性**：当输入事实错误时，skill 会按他的方式指出问题；历史回测能发现卡片缺陷。
4. **可扩展性**：新增第五个人时，流程是否还成立。

---

## Disclaimer / 免责声明

本 Skill 仅基于公开、可验证的思维框架做启发式模拟，**不构成**法律、财务、投资、税务或专业战略咨询。涉及高风险决策时，请咨询相应领域的专业人士。

This skill simulates publicly documented thinking frameworks for heuristic purposes only. It does **not** provide legal, financial, investment, tax, or professional strategic advice.

---

## License / 许可证

MIT

欢迎 Fork、扩展和添加你自己的“思维董事会”。
