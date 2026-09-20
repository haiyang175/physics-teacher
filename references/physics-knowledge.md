# 物理知识库（初中）

项目知识层中**经过人工核验**的条目。本文件替代了原先手写的初中错误概念表。

```yaml
provenance:
  - source_id: physics-teacher-agent-skills-knowledge
    source_name: physics-teacher-agent-skills knowledge
    source_url: 未记录（当前仓库未提供可核验 URL）
    license: 项目内部资料；外部再分发许可需核验
    version: misconception-seed-v0.2 / diagnostic-task-v0.3
    retrieved_at: 2026-09-18
    transformation: 人工核验后整理为本文件的概念卡、诊断任务卡与映射表
    attribution: physics-teacher-agent-skills
    verification_status: partial
  - source_id: qlm-labpath-k16-stem-misconceptions
    source_name: QLM LabPath K-16 STEM Misconceptions
    source_url: 未记录（当前仓库未提供可核验 URL）
    license: CC-BY-4.0（以原始资料许可为准，发布前需核验）
    version: 2026-09-18 import
    retrieved_at: 2026-09-18
    transformation: 仅保留可映射且标注 partial mapping 的条目，未映射记录不强行对应
    attribution: QLM LabPath
    verification_status: partial
```

> **范围**：目前**只有初中**。高中部分仍见 `physics-safety.md` 第四节的高中表。

---

## 一、前置知识图

诊断学情时**先查这里**：学生卡在某个概念上，往往不是这个概念本身，而是它的前置。

| 概念 | 需要的前置 |
|---|---|
| **浮力（`concept.buoyancy`）** | `concept.force`、压强（`concept.pressure`）、`concept.pressure-liquid`、`concept.force-analysis` |
| **压强（`concept.pressure`）** | `concept.force` |
| **`concept.pressure-liquid`** | 压强（`concept.pressure`） |
| **`concept.motion-force`** | `concept.force`、`concept.force-analysis` |
| **`concept.ohm-law`** | 电流（`concept.current`）、电压（`concept.voltage`）、电阻（`concept.resistance`） |
| **电功率（`concept.power`）** | `concept.energy`、电流（`concept.current`）、电压（`concept.voltage`） |

> **不在本表中的概念，前置关系尚未建立**——不要凭空推断，写「未建立」。

---

## 二、错误概念卡

每条含：学生的想法 → 科学模型 → 诊断证据 → 诊断任务 → 干预。
**字段与 `misconception_report` 模板一一对应**，可以先查这里，再结合本班情况补充。

### 浮力：物体受到浮力就一定漂浮，漂浮时浮力才等于物重。

**学生的想法**（`misconception.buoyancy.001`）
> 物体受到浮力就一定漂浮，漂浮时浮力才等于物重。

**正确的物理表述**
浮力是液体或气体对浸入物体的作用力；漂浮和悬浮且静止时，浮力与物重平衡，沉底、上浮等情况需依据完整受力状态判断。

**诊断证据**（学生表现出这些，说明可能持有该想法）
- 把‘有浮力’与‘漂浮’当作同义词
- 无法画出沉底物体仍受浮力的受力图

**诊断任务**
- 比较沉底、悬浮、漂浮三种状态并画受力图

**干预**
- 用弹簧测力计比较物体在空气中和液体中的示数
- 要求学生先说出平衡条件再判断浮力与重力关系

### 浮力：物体越重，受到的浮力一定越大。

**学生的想法**（`misconception.buoyancy.002`）
> 物体越重，受到的浮力一定越大。

**正确的物理表述**
浮力大小与排开液体或气体的情况及介质密度有关；在同一液体中不能只凭物体重力判断浮力，必须明确浸入体积、状态和条件。

**诊断证据**（学生表现出这些，说明可能持有该想法）
- 只比较物重，不比较排开液体体积或浸没状态

**诊断任务**
- 用同体积不同材料和同材料不同体积的物体进行对比

**干预**
- 先固定排开液体体积，再改变物重；随后交换控制变量

### 电流与电路：电流经过用电器后会被用掉，所以后面的电流更小。

**学生的想法**（`misconception.current.001`）
> 电流经过用电器后会被用掉，所以后面的电流更小。

**正确的物理表述**
在串联电路的稳恒状态下，各处电流相等；用电器转化的是电能等，不是把电流这种物理量‘消耗掉’。

**诊断证据**（学生表现出这些，说明可能持有该想法）
- 预测串联电路两个位置电流表示数不同
- 把灯泡亮度解释为电流被消耗

**诊断任务**
- 让学生预测并测量串联电路中两个位置的电流

**干预**
- 用电荷连续性和实测数据对照学生预测，区分电流与电能

### 电流与电压：电压就是电流的多少，电流越大电压就一定越大。

**学生的想法**（`misconception.current.002`）
> 电压就是电流的多少，电流越大电压就一定越大。

**正确的物理表述**
电压是两点间电势差，电流是电荷定向移动的物理量；二者关系要结合电路元件和条件分析，不能互相定义。

**诊断证据**（学生表现出这些，说明可能持有该想法）
- 把电压表读数当作电流表读数的另一种单位

**诊断任务**
- 分别判断电流表、电压表的连接位置和测量对象

**干预**
- 通过同一电路改变电阻，比较电流和电压的独立变化

### 压强：压力越大，压强一定越大。

**学生的想法**（`misconception.pressure.001`）
> 压力越大，压强一定越大。

**正确的物理表述**
压强由压力和受力面积共同决定；在受力面积不相同时，不能只比较压力。

**诊断证据**（学生表现出这些，说明可能持有该想法）
- 忽略鞋底面积、刀刃面积等情境中的受力面积

**诊断任务**
- 比较同一压力下不同受力面积的作用效果

**干预**
- 用海绵或软蜡块记录凹陷程度，明确控制变量

### 力与运动：物体要保持运动，必须一直受到沿运动方向的力。

**学生的想法**（`misconception.force-motion.001`）
> 物体要保持运动，必须一直受到沿运动方向的力。

**正确的物理表述**
力是改变物体运动状态的原因；在合力为零等条件下，物体可保持静止或匀速直线运动。

**诊断证据**（学生表现出这些，说明可能持有该想法）
- 把‘有运动’与‘有沿运动方向的力’直接绑定

**诊断任务**
- 比较冰面滑行、水平匀速运动和加速运动的受力情况

**干预**
- 先区分速度与合力，再用受力图解释运动状态变化

### 光学：反射角是反射光线与镜面的夹角。

**学生的想法**（`misconception.reflection.001`）
> 反射角是反射光线与镜面的夹角。

**正确的物理表述**
入射角和反射角都以法线为基准测量，反射角等于反射光线与法线的夹角。

**诊断证据**（学生表现出这些，说明可能持有该想法）
- 作图时把镜面作为角度基准

**诊断任务**
- 给出镜面、法线和光线，让学生分别标出两种角

**干预**
- 用可转动法线和量角器重新测量并比较

---

## 三、诊断任务卡

每条含：问题 → 期望回答 → 诊断信号 → 解读 → 干预 → 难度。
**这是 `diagnosis_report` 的成品级素材**，可直接改用。

### `diagnostic.pressure`（基础）

**目标概念**：压强（`concept.pressure`）　**前置概念**：`concept.force`

**针对的错误概念**：压力越大压强一定越大

**问题**
> 同样大小的压力作用在海绵的大面和小面上，哪个凹陷更深？为什么？

**期望回答**
能指出需要同时比较压力和受力面积

**诊断信号**（学生这样答 → 说明）
只说压力大的一组更深且不提面积

**解读**
可能混淆压力与压强并忽略控制变量

**干预**
用海绵和砝码完成先改压力后改面积的对照实验

### `diagnostic.buoyancy`（中等）

**目标概念**：浮力（`concept.buoyancy`）　**前置概念**：压强（`concept.pressure`）

**针对的错误概念**：浮力一定等于物重

**问题**
> 沉底的物体是否仍受浮力？漂浮时浮力为什么可能等于物重？

**期望回答**
能区分有浮力和漂浮平衡状态，并依据受力图判断

**诊断信号**（学生这样答 → 说明）
把有浮力直接等同于漂浮或认为沉底没有浮力

**解读**
可能缺少受力分析和状态条件意识

**干预**
用弹簧测力计比较空气中与液体中示数并画三种状态受力图

### `diagnostic.motion-force`（基础）

**目标概念**：`concept.motion-force`　**前置概念**：`concept.force`

**针对的错误概念**：运动需要持续有力维持

**问题**
> 冰面上的小车被推一下后，手离开小车它还能继续运动吗？若能，合力如何变化？

**期望回答**
能说出力改变运动状态而不是维持运动，合力接近零时可近似匀速

**诊断信号**（学生这样答 → 说明）
认为手停止施力物体立即停止

**解读**
可能持有力维持运动模型

**干预**
用低摩擦小车记录速度变化并配合受力图重建模型

### `diagnostic.current`（中等）

**目标概念**：`concept.circuit`　**前置概念**：电流（`concept.current`）

**针对的错误概念**：电流会被用电器用掉

**问题**
> 串联电路灯泡前后的电流表示数是否应不同？请先预测再说明理由。

**期望回答**
稳态串联电路各处电流在误差范围内相等，用电器转化能量而非消耗电流

**诊断信号**（学生这样答 → 说明）
预测后端电流更小并称电流被灯泡用掉

**解读**
可能混淆电流与电能

**干预**
实测串联电路不同位置电流并区分电流和电能

### `diagnostic.force-interaction`（基础）

**目标概念**：`concept.force`　**前置概念**：`concept.force`

**针对的错误概念**：力是物体自身具有的东西

**问题**
> 手推桌子时，桌子对手是否也有力？请指出相互作用的两个物体。

**期望回答**
能指出手和桌子相互作用且力成对出现

**诊断信号**（学生这样答 → 说明）
只说手对桌子有力而不承认反作用

**解读**
可能缺少相互作用观

**干预**
用弹簧测力计相连演示相互作用并标注施力物体和受力物体

---

## 四、概念卡要点

每个概念的**前置、表征、常见错误概念**。
**「表征」这一栏尤其重要**——学生答不上来，常常不是没记住结论，而是缺少某个表征。

| 概念 | 前置 | 常用表征 | 常见错误概念 |
|---|---|---|---|
| **浮力** | 压力、压强、力的测量 | 受力图、弹簧测力计示数差、排开液体体积 | 浮力一定等于物重；物体越重浮力一定越大 |
| **压强** | 力、面积、单位换算 | 受力面示意图、公式 p=F/S、压强大小规律 | 压力越大压强一定越大；压强就是压力 |
| **电流** | 简单电路、电荷 | 电路图、电流表读数、电流方向约定 | 电流会被用掉；电流从正极流出后越来越少 |
| **电压** | 简单电路、电流 | 电路图、电压表接法、电势差类比 | 电压就是电流；电压表应串联 |
| **电阻** | 电流、电压、单位 | 伏安特性、电路图、R=U/I | 电阻越大电流一定越大；电阻是导体中被消耗的东西 |
| **速度** | 路程、时间、单位换算 | s-t图像、v-t图像、平均速度公式 | 速度越大通过的路程一定越长；平均速度是各时刻速度的简单平均 |
| **滑动摩擦力** | 力的方向、相对运动、控制变量 | 受力图、弹簧测力计示数、实验数据表 | 摩擦力方向永远与物体运动方向相反；摩擦力越大物体运动越快 |
| **电功率** | 电流、电压、能量与功 | 铭牌、P-t图像、电功率公式 | 额定功率就是实际功率；功率越大用电时间一定越短 |
| **光的反射** | 光沿直线传播、角度测量 | 光路图、平面镜成像图、法线 | 反射角是光线与镜面的夹角；所有表面反射方向都相同 |

---

## 五、QLM 错误概念映射

QLM 数据集条目 → 本项目概念的映射。数据集自标为「partial mapping」，
**未映射的记录没有被强行对应**——遇到不确定的，就说不确定。

| QLM 条目 | 目标概念 | 错误概念类型 | 诊断任务 | 干预 |
|---|---|---|---|---|
| `phys-mech-heavy-objects-sink-light-float` | `concept.buoyancy` | density-weight-confusion | `diagnostic.buoyancy` | clay-boat-and-density-comparison |
| `phys-mech-gravity-needs-medium` | `concept.force` | force-medium-confusion | `diagnostic.force-interaction` | force-and-field-model |
| `phys-mech-friction-always-bad` | `concept.motion-force` | friction-value-judgment | `diagnostic.motion-force` | friction-use-cases |
| `phys-mech-mass-affects-fall-speed` | `concept.motion-force` | mass-fall-speed | `diagnostic.motion-force` | controlled-fall-comparison |
| `phys-mech-force-in-direction-of-motion` | `concept.motion-force` | force-direction | `diagnostic.motion-force` | force-velocity-vector-analysis |
| `phys-energy-renewable-means-infinite` | `concept.energy` | energy-resource-confusion | `diagnostic.motion-force` | energy-flow-and-efficiency |
| `phys-energy-work-means-effort` | `concept.work-energy` | work-effort-confusion | `diagnostic.motion-force` | displacement-and-work-cases |
| `phys-elec-bigger-battery-more-current` | `concept.current` | current-voltage-confusion | `diagnostic.current` | battery-voltage-resistance-comparison |
| `phys-optics-we-see-light-beams` | `concept.light` | light-ray-observation | `diagnostic.force-interaction` | scattering-demonstration |
| `phys-thermo-temperature-determines-phase` | `concept.phase-change` | temperature-only-phase | `diagnostic.pressure` | pressure-temperature-phase-comparison |

---

## 六、使用约定

- 本文件是**素材库，不是答案**：查到条目后仍要结合教师提供的学情作答与本校教材调整。
- **没有对应条目就说没有**：本库只覆盖初中的部分主题，高中尚未建立。
- 引用此处内容**不必标注出处**（项目自有数据）；但**不得**据此编造课标条款、教材页码或文献。
- 数据更新时同步更新本文件，**不要在别处再抄一份**。

## 七、统一知识条目结构

新增或迁移条目时，优先使用以下字段；现有叙述式卡片按主题逐步迁移，不为迁移而虚构缺失信息：

```yaml
concept:
grade:
topic:
prerequisites:
core_statement:
representations:
common_misconceptions:
diagnostic_signals:
diagnostic_tasks:
interventions:
experiments:
boundary_conditions:
related_concepts:
provenance:
```

其中 `boundary_conditions` 必须写明结论的适用条件、理想化或不能外推的范围；没有可靠信息时写「未建立」，不猜测。

迁移示例（仅示意字段，不替代上面的核验卡）：

```yaml
concept: buoyancy
grade: 初中
topic: 浮力
prerequisites: [force, pressure, pressure-liquid]
core_statement: 浮力取决于排开介质的情况与介质密度，不能只由物重判断
representations: [受力图, 测力计示数差, 排开液体体积]
common_misconceptions: [物体越重浮力一定越大]
diagnostic_signals: [只比较物重而忽略排开体积]
diagnostic_tasks: [同体积不同材料与同材料不同体积对比]
interventions: [先固定排开体积，再交换控制变量]
experiments: [测力计与溢水杯对比实验]
boundary_conditions: 同一液体、测量范围和仪器精度内；不外推到未控制密度或状态的情形
related_concepts: [pressure, force-analysis]
provenance: qlm-labpath-k16-stem-misconceptions / partial mapping
```
