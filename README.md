# W-ABCD 真假 Web3 识别器 · `wabcd-identifier`

> **帮普通用户一眼识破"打着 Web3 旗号的伪项目 / 资金盘"，降低受骗风险。**

一个项目满嘴"AI + 区块链 + 大数据 + 共建社区"，它到底是**真·Web3 产业应用**，还是只是套了层区块链壳的**伪概念 / 资金盘**？这个 skill 把《价值互联网产业应用蓝皮书（2025）》里的 **W-ABCD 范式**变成人人能用的"真伪滤镜"，三问就能戳破包装。

---

## 为什么需要它

- 市面上大量"我们用 AI+区块链+大数据打造产业 Web3"的宣传，真假难辨。
- 很多是**伪 Web3**，甚至就是**资金盘骗局**（冒牌交易所、合约跟单盘、拉人头返利盘）。
- 普通用户缺乏判别工具，极易在高收益话术下踩坑。
- 本 skill 把学术范式变成可操作的核对清单，**不依赖专业知识也能用**。

---

## 核心方法论：W-ABCD 五要素

| 要素 | 含义 | 你要核对的证据 |
|------|------|----------------|
| **W** Web3 价值网络 | 内核是否"传递价值、计量贡献并分配"（不是只传信息） | 有没有贡献计量 + 分配机制 |
| **A** AI / AIoT | 是否当新质生产工具，提升贡献可度量性 | AI 是噱头还是真工具 |
| **B** Blockchain | 是否作可信底座（存证/不可篡改/溯源/自动执行） | 链上不可篡改 + 智能合约 |
| **C** 共建社区 | 成员"消费即投资、行动贡献即投资"，通证是计量工具非纯积分 | **关键变量，下面细说** |
| **D** Data 数据要素 | 实体运营数据是否变成可信、可定价的生产要素闭环 | 数据有没有上链定价 |

**C（共建社区）是试金石。** 只把技术当栈堆砌、**没有真实的共建社区**，那就是信息化升级，不是真 Web3。

### C 验真三问（普通用户也能问）
1. 成员是否"消费即投资 / 行动贡献即投资"？
2. 通证是否用于**计量分配**而非纯积分？
3. 治理是否**多方共治**而非中心化分发？

三问过不了（比如只是个粉丝群发积分、拉人头返利）→ 直接判**伪 Web3 / 疑似资金盘**。

---

## 快速开始

### 方式一：从 GitHub 安装（推荐）
```bash
git clone https://github.com/<你的用户名>/web3-wabcd-identifier.git
cp -r web3-wabcd-identifier/wabcd-identifier ~/.workbuddy/skills/
```
重启 WorkBuddy 后，对话中只要出现"这个项目算真 Web3 吗""是不是资金盘"等信号即可自动激活。

### 方式二：从 WorkBuddy 技能市场安装
> 市场发布后在此填写一键安装命令 / 链接。

### 方式三：手动安装
把本仓库的 `wabcd-identifier/` 目录整体复制到用户目录下的 `.workbuddy/skills/` 即可（Windows 为 `%USERPROFILE%\.workbuddy\skills\`）。

### 验证安装
```bash
ls ~/.workbuddy/skills/wabcd-identifier/SKILL.md   # 存在即安装成功
```

---

## 使用示例

### 示例 1 — 交易所是不是 Web3？
> 用户："区块链+大数据就是 Web3 吗？我们老板说上了链就是 Web3。"

skill 激活后逐项核对：B（有链）存在，但核心交易撮合是中心化的、**C（真实共建社区）缺失** → 结论：有区块链零件但不是产业 Web3，属金融交易场所。详见 [`examples/example-1-exchange.md`](wabcd-identifier/examples/example-1-exchange.md)。

### 示例 2 — 某"协作型交易所"是资金盘吗？
> 用户："有个叫币燃 BURNEX 的，说协作交易、共建社区，靠谱吗？"

逐项核对发现：核心是**后台操控的封闭资金池**（非真实交易）、C 是拉人头话术、已被多个反诈骗渠道预警"即将崩盘跑路" → 结论：**伪 Web3 + 资金盘，勿参与**。详见 [`examples/example-2-burnex.md`](wabcd-identifier/examples/example-2-burnex.md)。

### 示例 3 — "宣称有社区" vs "真有共建社区"
> 用户："它说自己有共建社区，但真的吗？"

按 C 验真三问核对：是粉丝群发积分、中心化决策 → 缺真实共治 → 判伪。详见 [`examples/example-3-community.md`](wabcd-identifier/examples/example-3-community.md)。

---

## 与相邻 skill 的关系

| 相邻 skill | 关系 | 说明 |
|-----------|------|------|
| `token-concept-disambiguator`（S1 概念辨析器） | depends-on | 真伪识别前先厘清概念层级（通证化/代币化/RWA） |
| `three-mode-classifier`（S3 模式判别器） | contrasts-with | S4 定真伪，S3 定"原生型/产业变革型/链改型"选型 |
| `risk-assessment-antipattern`（S7 风险评估反例库） | composes-with | 真伪识别后进一步三层体检、筛伪 RWA |

**推荐顺序**：S1（概念）→ S4（真伪）→ S3/S8（模式/路径）→ S7（风险）。

---

## 边界（什么时候不用本 skill）

- 只想搞清"通证化/代币化/RWA"概念区别 → 用 **S1**。
- 已确认真 Web3，要选主导模式/落地路径 → 用 **S3 / S8**。
- 纯政策条文查询 → 不在本 skill 范围。

---

## 质量与测试

- 经 cangjie-distill 流水线阶段 1.5 三重验证（V1 跨域 / V2 预测力 / V3 独特性）通过。
- 含 `test-prompts.json` 压力测试集（4 条 should_trigger + 3 条 should_not_trigger 诱饵 + 2 条 edge_case），诱饵容错为 0。
- `test-results.md` 实测通过率 **100%**。

---

## 来源与版权

- **方法论来源**：《价值互联网产业应用蓝皮书（2025）》编写组（导言 / 第一章 W-ABCD 范式）。R 段原文引用已署名，请遵守原著版权，合理使用。
- **蒸馏流水线**：[cangjie-distill](https://lightmake.site)（SkillHub: keen / sanbu）。
- **授权**：本仓库的 skill 结构、改写与文档以 **Apache-2.0** 授权（见 `LICENSE`）。Apache-2.0 **仅覆盖本仓库的结构与改写**，不覆盖蓝皮书原著内容。
- **免责声明**：本 skill 仅供识别参考，**不构成任何投资建议**。涉及中国大陆境内虚拟货币交易、交易所相关业务属非法金融活动，请勿参与。

---

## 许可证

[Apache-2.0](LICENSE)
