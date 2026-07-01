# Decision Log / 决策日志

本文件记录两类内容：
1. **历史回测（Backtests）**：用重大商业决策验证 `MINDS.md` 中思维卡片的准确性。
2. **用户决策日志（User Decision Log）**：用户可用 `TEMPLATES/decision-trace-template.md` 记录自己的重大决策，以便日后复盘。

---

## 回测目录

- [BACKTEST-001: iPhone 取消物理键盘（2007）](#backtest-001-iphone-取消物理键盘2007)
- [BACKTEST-002: Amazon Prime 推出（2005）](#backtest-002-amazon-prime-推出2005)
- [BACKTEST-003: Tesla Model 3 垂直整合与产能地狱（2017–2018）](#backtest-003-tesla-model-3-垂直整合与产能地狱20172018)
- [BACKTEST-004: NVIDIA CUDA 投资（2006–2016）](#backtest-004-nvidia-cuda-投资20062016)

---

## BACKTEST-001: iPhone 取消物理键盘（2007）

- **决策者 / Thinker(s) invoked**: Council（Jobs / Musk / Bezos / Huang）
- **决策背景 / Context**:
  - 2005–2006 年，手机市场由黑莓、Palm、诺基亚主导，物理键盘是“行业标准”。
  - 苹果内部对是否保留物理键盘有激烈争论。
  - iPod 成功让苹果有现金和品牌底气押注新品类。
- **当时的问题 / Question at the time**: 智能手机是否应该保留物理键盘以确保输入效率和市场接受度？
- **历史实际选择 / Actual historical decision**: 取消物理键盘，押注全触屏 + 多点触控 + 虚拟键盘。

### 参谋团预测 / Council Predictions

- **Steve Jobs 视角**: 坚持取消。核心问题是“用户第一次拿起手机的‘哇’时刻是什么”。物理键盘会固化设备形态，限制软件创新。整体体验 > 功能堆砌。
- **Elon Musk 视角**: 如果触控在物理上可达到足够延迟与准确率，就应放弃机械部件。成本结构也会更优。但需要快速迭代虚拟键盘的输入体验。
- **Jeff Bezos 视角**: 这是 Type 1 单向门决策，应小范围用户测试后再定。但若测试显示用户能接受虚拟键盘，长期客户飞轮（App 生态）将远超短期输入效率损失。
- **Jensen Huang 视角**: 这是在定义“移动计算”这个新市场，而不是在现有手机市场抢份额。平台生态（App Store）比单品更重要。

### 结果 / Outcome

- **短期结果（0-12 个月）**: 市场对虚拟键盘有质疑，但多点触控带来颠覆性体验，iPhone 成为现象级产品。
- **中期结果（1-3 年）**: App Store 生态爆发，虚拟键盘输入体验持续优化，物理键盘手机迅速边缘化。
- **长期结果（3 年以上）**: 重新定义智能手机品类，触屏成为行业标准。

### 可修正性记录 / Correctability Notes

- **一致点**: Jobs 的“整体体验 > 功能堆砌”、Huang 的“平台/生态 > 单品”与历史结果高度一致。
- **补充点**: Bezos 的“小范围测试”提醒我们在真实决策中应降低单向门风险；Musk 的“物理可行性”提醒虚拟键盘必须达到可用阈值。
- **卡片更新建议**: 在 Jobs 的 `WholeWidget` 模型中强化“硬件形态必须服务于软件体验上限”这一边界；在 Huang 的 `ZeroBillionMarket` 中补充“创造新市场需要配套生态”的案例。

### 来源 / Sources

- 《Steve Jobs》(Walter Isaacson)
- Apple iPhone 2007 发布会
- 公开访谈与产品设计回顾

---

## BACKTEST-002: Amazon Prime 推出（2005）

- **决策者 / Thinker(s) invoked**: Council
- **决策背景 / Context**:
  - 2005 年亚马逊现金流紧张，华尔街要求盈利。
  - 物流成本高昂，免费两日达意味着短期巨额亏损。
  - 电商竞争激烈，客户忠诚度低。
- **当时的问题 / Question at the time**: 是否应推出每年 79 美元的会员服务，提供免费两日达，以短期亏损换取长期客户忠诚？
- **历史实际选择 / Actual historical decision**: 推出 Amazon Prime。

### 参谋团预测 / Council Predictions

- **Steve Jobs 视角**: 如果能让用户感到“被宠爱”，值得做；但需控制体验端，确保履约质量不会损害品牌。
- **Elon Musk 视角**: 先计算物流网络在物理上能否支撑；如果 unit economics 在规模化后可行，就值得做。
- **Jeff Bezos 视角**: 强烈支持。这是长期客户信任 > 短期利润的经典应用，也是客户飞轮的关键加速器。
- **Jensen Huang 视角**: 不要把 Prime 当作单品，而要把它做成平台飞轮入口。会员体系一旦形成，竞争门槛极高。

### 结果 / Outcome

- **短期结果（0-12 个月）**: 会员数增长迅速，但物流成本大幅上升，短期利润承压。
- **中期结果（1-3 年）**: Prime 会员购买频次和客单价显著高于非会员，飞轮开始转动。
- **长期结果（3 年以上）**: 数亿会员，成为亚马逊生态核心，支撑了 AWS、视频、广告等后续业务。

### 可修正性记录 / Correctability Notes

- **一致点**: Bezos 的“客户飞轮”和“长期 > 短期”完美预测了 Prime 的成功逻辑。
- **补充点**: Jobs 提醒体验控制；Musk 提醒 unit economics；Huang 提醒平台入口思维。
- **卡片更新建议**: 在 Bezos 的 `CustomerFlywheel` 中补充 Prime 作为“付费锁定客户忠诚”的变体；在 Huang 的 `AcceleratedComputingPlatform` 中类比“会员体系也是一种平台”。

### 来源 / Sources

- Amazon 2005–2007 股东信
- 《The Everything Store》(Brad Stone)
- 公开访谈

---

## BACKTEST-003: Tesla Model 3 垂直整合与产能地狱（2017–2018）

- **决策者 / Thinker(s) invoked**: Council
- **决策背景 / Context**:
  - 2017 年 Model 3 开始量产，但产能远低于预期。
  - 空头围攻，现金极度紧张，公司濒临破产。
  - 马斯克决定睡在工厂，逐条产线重构制造流程。
- **当时的问题 / Question at the time**: 在产能地狱中，是应该继续垂直整合自研零部件，还是外包给成熟供应商以快速放量？
- **历史实际选择 / Actual historical decision**: 坚持垂直整合 + 瓶颈优先 + 快速迭代，最终突破周产 5000 辆目标。

### 参谋团预测 / Council Predictions

- **Steve Jobs 视角**: 如果外包会损害产品体验和品牌控制，应坚持自研；但不要让制造危机拖垮公司生存。
- **Elon Musk 视角**: 强烈支持垂直整合。瓶颈是产线本身，必须用五步算法和瓶颈优先解决；外包只是把瓶颈转移给供应商。
- **Jeff Bezos 视角**: 这是 Type 1 生存决策，先止血。可以在某些非核心零部件上短期外包，但核心电池/电机必须控制。
- **Jensen Huang 视角**: 不要只看单车产能，要看平台能力。垂直整合是在构建长期制造平台，但必须有足够现金活到平台成熟。

### 结果 / Outcome

- **短期结果（0-12 个月）**: 产能缓慢爬坡，公司现金压力巨大，马斯克个人承受极限压力。
- **中期结果（1-3 年）**: Model 3 成为全球最畅销电动车，特斯拉实现规模化盈利。
- **长期结果（3 年以上）**: 垂直整合能力成为特斯拉成本优势和迭代速度的核心。

### 可修正性记录 / Correctability Notes

- **一致点**: Musk 的“瓶颈优先”和“五步算法”与历史选择高度一致。
- **补充点**: Bezos 提醒这是 Type 1 生存决策，Huang 提醒平台视角和现金耐力。
- **卡片更新建议**: 在 Musk 的 `BottleneckFirst` 中补充“瓶颈可能在内部也可能在外包商”的边界；在 Bezos 的 `OneWayTwoWayDoors` 中补充“生存危机可能把 reversible 决策变成 de facto 不可逆”。

### 来源 / Sources

- 《Elon Musk》(Walter Isaacson)
- Tesla 2017–2018 财报电话会
- 公开访谈与纪录片

---

## BACKTEST-004: NVIDIA CUDA 投资（2006–2016）

- **决策者 / Thinker(s) invoked**: Council
- **决策背景 / Context**:
  - 2006 年 NVIDIA 发布 CUDA，希望让 GPU 用于通用计算。
  - 当时 GPU 通用计算市场几乎不存在，华尔街质疑投资回报。
  - NVIDIA 持续投入十年，直到 2016 年深度学习爆发。
- **当时的问题 / Question at the time**: 是否应该持续投资 CUDA 和 GPU 通用计算生态，即使未来 5-10 年看不到大规模商业化回报？
- **历史实际选择 / Actual historical decision**: 持续投资 CUDA，建立开发者生态，最终成为 AI 基础设施。

### 参谋团预测 / Council Predictions

- **Steve Jobs 视角**: 如果 CUDA 能带来“不可思议”的计算体验，值得做；但需要找到第一个能让用户 wow 的应用场景。
- **Elon Musk 视角**: 从第一性原理看，并行计算的物理效率远超 CPU，只要应用场景出现，需求会爆发。
- **Jeff Bezos 视角**: 这是典型的长期 > 短期决策，但必须控制投入节奏，确保核心游戏业务能提供现金流。
- **Jensen Huang 视角**: 强烈支持。这是零亿美元市场和加速计算平台的结合；如果我们不建 CUDA，客户永远不会来。

### 结果 / Outcome

- **短期结果（0-12 个月）**: CUDA 开发者数量有限，收入贡献微不足道。
- **中期结果（1-3 年）**: 高性能计算、加密货币矿机、早期深度学习开始采用 GPU。
- **长期结果（3 年以上）**: 2016 年后深度学习爆发，CUDA 成为 AI 基础设施标准，NVIDIA 成为万亿公司。

### 可修正性记录 / Correctability Notes

- **一致点**: Huang 的“零亿美元市场”和“加速计算平台”完美解释了 CUDA 战略。
- **补充点**: Musk 从物理效率角度支持；Bezos 提醒现金流管理；Jobs 提醒需要找到 wow 场景。
- **卡片更新建议**: 在 Huang 的 `ZeroBillionMarket` 中补充“必须同时投资生态和等待杀手级应用”；在 `AcceleratedComputingPlatform` 中补充“CUDA 需要核心游戏业务提供现金流”的边界。

### 来源 / Sources

- NVIDIA 公开演讲与股东大会
- Acquired 专访
- 公开技术文档与行业分析

---

## 如何记录新的用户决策

当你要用这个 skill 为自己的重大决策建立追溯条目时，可以这样说：

```text
/business-council
请帮我为以下决策建立一个决策追溯条目：
[决策背景]
[问题]
[我正在考虑的选择]
[当前已知约束]
```

Agent 会按 `TEMPLATES/decision-trace-template.md` 输出，并建议是否更新相关思维卡片。

---

## 记录原则

1. **情境优先**：必须还原当时的约束，不能用后见之明替代当时的判断。
2. **来源可考**：每个关键事实都要能追溯到公开资料。
3. **诚实标记**：明确区分“事实”、“合理推断”和“反向推演”。
4. **行动导向**：每次回测都应产生至少一条对思维卡片的修正建议。
