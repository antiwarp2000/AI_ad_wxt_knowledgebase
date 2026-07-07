# AI 策略知识库索引

## 快速入口

| 任务 | 入口文件 |
|---|---|
| 看指标怎么算 | `01_metrics_dictionary/metrics_dictionary.md` |
| 判断计划分层 | `02_rules_engine/plan_tier_rules.yaml` |
| 判断计划健康度 | `02_rules_engine/health_score_rules.yaml` |
| 找异常根因 | `03_decision_trees/diagnosis_decision_tree.md` |
| 查策略/SOP/经验 | `04_strategy_docs/` |
| 查历史经验 | `05_case_library/` |
| 生成动作清单 | `06_action_playbooks/action_playbooks.md` |
| 对接 AI Agent | `07_agent_io_schema/` |
| 每日复盘 | `08_review_logs/daily_review_template.md` |

## 推荐 AI 调用顺序

1. 读取输入计划数据。
2. 按指标字典计算 ROI、CTR、CVR、CPC、CPA。
3. 用 `plan_tier_rules.yaml` 判断计划分层。
4. 用 `diagnosis_decision_tree.md` 找根因路径。
5. 按诊断标签读取 `04_strategy_docs` 里的对应策略文档。
6. 从 `05_case_library` 查相似案例。
7. 用 `06_action_playbooks` 生成动作清单。
8. 把执行结果写入 `08_review_logs`，成熟案例沉淀到 `05_case_library`。

## 常见诊断路由

| 诊断问题 | 先看规则 | 再看归因 | 补充策略 |
|---|---|---|---|
| 计划分层不准 | `02_rules_engine/plan_tier_rules.yaml` | - | `05_case_library/` |
| ROI 下滑 | `02_rules_engine/health_score_rules.yaml` | `03_decision_trees/diagnosis_decision_tree.md` | `04_strategy_docs/04_投后优化阶段.md` |
| 有点击无转化 | `02_rules_engine/plan_tier_rules.yaml` | `03_decision_trees/diagnosis_decision_tree.md` | `04_strategy_docs/09_常见问题与解决方案.md` |
| 新品投放 | - | - | `04_strategy_docs/02_投前准备阶段.md`、`04_strategy_docs/08_各场景投放策略.md` |
| 投放动作生成 | `02_rules_engine/plan_tier_rules.yaml` | `03_decision_trees/diagnosis_decision_tree.md` | `06_action_playbooks/action_playbooks.md` |
