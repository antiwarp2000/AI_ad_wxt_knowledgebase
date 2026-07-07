# 万相台 AI 投放知识库

这是用于沉淀万相台广告投放策略的轻量结构化知识库。当前版本不依赖向量索引，核心目标是用稳定、可维护的方式支持广告计划诊断。

## 核心方法

```text
算指标 -> 套规则 -> 做归因 -> 查策略文档 -> 参考案例 -> 给动作 -> 复盘沉淀
```

## 目录入口

- `ai_strategy_knowledge_base/`：结构化 AI 策略知识库主目录
- `知识库新手维护指南.md`：给不熟悉知识库的人使用的维护说明
- `ai_strategy_knowledge_base/index.md`：AI 调用索引
- `ai_strategy_knowledge_base/README.md`：知识库设计说明

## 知识库结构

| 目录 | 用途 |
|---|---|
| `00_raw_sources` | 原始万相台投放资料归档 |
| `01_metrics_dictionary` | ROI、CTR、CVR、CPC 等指标口径 |
| `02_rules_engine` | 黄金/潜力/止损/问题计划分层规则 |
| `03_decision_trees` | 无展现、无点击、无转化、ROI 下滑等异常归因 |
| `04_strategy_docs` | SOP、策略说明、经验文档，按目录/文件名直接读取 |
| `05_case_library` | 历史案例模板与投放经验沉淀 |
| `06_action_playbooks` | 诊断后的运营动作剧本 |
| `07_agent_io_schema` | 后续接入 AI Agent/看板的输入输出结构 |
| `08_review_logs` | 每日复盘和规则校准记录 |

## 推荐使用方式

1. 看板或 Agent 先读取计划数据并计算指标。
2. 使用 `02_rules_engine` 判断计划分层。
3. 使用 `03_decision_trees` 做异常归因。
4. 按诊断标签读取 `04_strategy_docs` 里的策略文档。
5. 使用 `05_case_library` 匹配历史经验。
6. 使用 `06_action_playbooks` 输出运营动作。
7. 把执行结果写回 `08_review_logs` 和案例库。

## 维护原则

- 关键判断放规则库，不要只藏在长文本里。
- 策略文档负责解释和方法，不负责最终裁判。
- 每次真实投放调整后，尽量补一条案例。
- 每周小幅校准规则，不要一次大改。
