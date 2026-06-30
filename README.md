# Business Council / 商业思维参谋

[![Claude Code Skill](https://img.shields.io/badge/Claude%20Code-Skill-blue)](https://claude.ai/code)

A Claude Code skill that simulates the business thinking of **Steve Jobs**, **Elon Musk**, **Jeff Bezos**, and **Jensen Huang** to advise on strategy, product, go-to-market, capital allocation, organization, and crisis decisions.

一个用于 Claude Code 的 skill，模拟**史蒂夫·乔布斯、埃隆·马斯克、杰夫·贝索斯、黄仁勋**四位企业家的思维方式，为商业决策提供多角度参谋。

---

## What it does / 功能简介

When you invoke this skill with a business question, it channels four distinct minds and gives you:

- A **restatement** of your problem and its core category
- **Four perspective analyses** (Jobs / Musk / Bezos / Huang)
- A **synthesized recommendation** with trade-offs and action items
- A **risk reminder** and disclaimer

当你向 skill 提出一个商业问题时，它会从四位企业家的视角给出结构化分析，并综合成可执行的建议。

---

## Installation / 安装

### Option 1: Copy into your project / 复制到项目

```bash
cd your-project
mkdir -p .claude/skills
git clone git@github.com:GresonKwan/business-council-skill.git .claude/skills/business-council
```

### Option 2: Add as a Git submodule / 作为子模块添加

```bash
cd your-project
mkdir -p .claude/skills
git submodule add git@github.com:GresonKwan/business-council-skill.git .claude/skills/business-council
```

Then restart or reload Claude Code to pick up the skill.

然后重启或重新加载 Claude Code 以识别 skill。

---

## Usage / 使用

Invoke the skill with `/business-council` followed by your question:

```text
/business-council 我该进入哪个市场？
/business-council 我的 SaaS 产品应该加这个功能吗？
/business-council 账上有 1500 万，应该怎么分配？
```

### Modes / 调用模式

| Mode | Trigger | Description |
|---|---|---|
| **Council Mode** | Just ask a question | 四位企业家共同分析并给出综合建议 |
| **Single Mind** | `@Jobs`, `@Musk`, `@Bezos`, `@Huang` | 只以指定企业家视角回答 |
| **Debate Mode** | `debate` or `辩论` | 四位企业家就同一问题展开辩论 |
| **Add-Mind Mode** | `add-mind <person>` | 提取新人物的思维模型卡片 |

### Examples / 示例

```text
/business-council @Musk 如何降低制造成本？
/business-council debate 应该先发布 imperfect 产品还是等完美？
/business-council add-mind Warren Buffett
```

---

## File Structure / 文件结构

```text
.
├── SKILL.md      # Skill manifest & system prompt / Skill 主配置与系统提示
├── MINDS.md      # Mind cards of the four thinkers / 四位企业家思维模型卡片
├── ADD_MIND.md   # Framework for adding new thinkers / 新增人物提取框架
├── EXAMPLES.md   # Output examples / 输出示例
├── README.md     # This file
└── .gitignore
```

---

## Adding New Thinkers / 添加新人物

Use Add-Mind mode to extract a new mind card:

```text
/business-council add-mind <人物名>
```

The skill will ask for source materials, search the web if needed, and output a draft card following the framework in `ADD_MIND.md`. You can then append it to `MINDS.md` and update `SKILL.md`.

---

## Disclaimer / 免责声明

This skill simulates publicly documented thinking frameworks for heuristic purposes only. It does **not** provide legal, financial, medical, or professional strategic advice. Always consult qualified professionals for high-stakes decisions.

本 skill 仅模拟四位企业家的公开思维框架，用于启发式思考，**不构成**法律、财务或专业战略咨询。涉及重大决策时，请咨询相关专业人士。

---

## License / 许可证

MIT

Feel free to fork, extend, and add your own minds.
