# Task Routing

这是轻量级任务选择规则，不是 Agent Router。先看输入材料，再看教师目的；若两者冲突，以材料门禁为准。

| 输入材料 | 教师目的 | 任务 |
|---|---|---|
| 学生实际表现（答题、口述、课堂行为） | 判断哪里没学会 | `diagnosis_report` |
| 学生错误想法或原话，但没有具体作答过程 | 分析可能的错误概念 | `misconception_report` |
| 完整题干 + 学生实际作答 | 分析这一次具体错误 | `error_analysis_report` |
| 教案原文（至少有教学目标与流程） | 找问题、评估设计 | `lesson_design_review` |
| 教案原文 + 明确要求修改 | 修改原教案 | `lesson_plan_revision`（先做必要的 `lesson_design_review`） |
| 教师提出导入、活动、难点或取舍困惑 | 给方向与决策支持 | `design_coaching` |

## 选择规则

1. 有学生实际作答时，优先 `error_analysis_report`；不要把一次具体错误改写成泛泛的 `misconception_report`。
2. 没有实际作答时，可以做 `diagnosis_report` 的通用诊断工具或 `misconception_report`，但必须标明不能形成针对该生的确定性诊断。
3. 只有学生表现、没有错误原话时，优先 `diagnosis_report`；只有错误原话、没有表现证据时，优先 `misconception_report`。
4. 只有教案且教师问“有什么问题”，用 `lesson_design_review`；教师明确说“请改写/压缩/降低难度”，用 `lesson_plan_revision`。
5. 教师只要思路、方向或取舍时，用 `design_coaching`，不给完整教案。
6. 材料不足时，先指出缺口及其影响，再给仍然可做的部分；不能用通用模板冒充完成了具体任务。

## 相邻任务的输出边界

- `diagnosis_report`：判断需要进一步区分的理解状态，并给出可验证的诊断任务。
- `misconception_report`：解释错误模型、暴露它的证据和纠正路径；不能声称该生一定持有该模型。
- `error_analysis_report`：逐步对应题干与作答，定位这一次具体错误，并给出验证是否改正的办法。
- `lesson_design_review`：指出原教案的问题、证据和优先级，不直接重写全文。
- `lesson_plan_revision`：在保留可取设计的前提下给出修订稿，并列明改动与仍存问题。
- `design_coaching`：给多个方向、依赖条件和取舍，让教师继续做设计决策。
