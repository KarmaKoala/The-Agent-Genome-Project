# Agent基因组计划 (AGP) v2.1

![Version](https://img.shields.io/badge/version-v2.1-blue)
![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)
![Status](https://img.shields.io/badge/status-stable-brightgreen)

The Agent Genome Project (AGP): The open-source engineering blueprint for defining the core capabilities, boundaries, and ethics of any AI agent.

## 📖 这是什么？(What is AGP?)

AGP，全称**智能体基因组计划 (The Agent Genome Project)**，是一个开源的、标准化的工程规范，旨在为AI智能体（AI Agent）的构思、设计与构建提供一套完整的基础蓝图。

本协议基于对智能体的正式定义：**智能体是一个能够感知环境、做出决策并采取行动以实现特定目标的智能系统，其关键特征包括自主性、适应性和与其环境的互动性。**

我们之所以称之为“**基因组 (Genome)**”，是因为这个协议的核心思想，是为每一个符合上述定义的AI智能体提供一套完整的“遗传指令集”。就像生物体的DNA决定了其形态、能力和天性一样，AGP通过一系列精确的“基因”（即协议中的属性），来编码构成一个Agent的所有核心特性。

AGP将每个Agent的定义档案（ADP）最终表达为一个清晰的**基因序列 (Genetic Sequence)**——一个由 `-` 分隔的、代表其三层能力的数字串。这个序列就是Agent独一无二的“数字指纹”。

## 🎯 我们要解决的问题 (The Problem)

在当前AI Agent开发的浪潮中，开发者和产品经理正面临一系列严峻的挑战，这些挑战系统性地阻碍了项目的效率、安全性和可扩展性：

* **定义模糊 (Vague Definitions)**: “智能助理”、“任务机器人”等标签过于宽泛，团队内部对于Agent的核心特性缺乏统一、精确的认知，导致沟通不畅和需求错位。
* **边界失控 (Uncontrolled Boundaries)**: 开发者很难清晰地界定Agent的行动范围和决策权限。这不仅带来安全风险，也使得Agent的行为难以预测和管理。
* **成本高昂 (High Costs)**: Agent定义不明确，导致底层大语言模型（LLM）需要执行大量不必要的“思考”，这会急剧增加Token消耗，造成严重的成本超支和性能下降。
* **选型困难 (Difficult Model Selection)**: 面对GPT, Gemini, Claude等众多模型，如何选择最适合当前Agent需求的、兼具性能和成本效益的底层模型，是一个复杂且重要的决策。

## 💡 我们的解决方案 (The Solution)

AGP通过提供一套标准化的设计和沟通框架，直接应对上述挑战：

* **基因序列定义 (Genetic Sequence Definition)**: AGP提供了一个由三个逻辑层构成的档案，将模糊的概念（如“智能”）分解为28个具体的、可量化的核心属性，并最终形成一个清晰的数字“基因序列”。
* **清晰的能力边界 (Clear Capability Boundaries)**: 通过对自主性(`autonomy`)、知识边界(`knowledge_boundary`)和风险偏好(`risk_adversity`)等关键属性的精确分级和断言，AGP为Agent设定了可量化、可测试、可验证的安全护栏。
* **成本效益导向 (Cost-Effective by Design)**: 清晰的定义使得开发者可以为不同复杂度的任务匹配恰当智能水平的Agent。例如，一个仅需基础因果推理（`cognitive_logic: 0`）的诊断Agent，可能通过一个经过微调的、成本更低的小模型就能实现，而无需动用为处理高度抽象问题（`cognitive_logic: 1`）设计的、最昂贵的前沿大模型，从而在设计源头就实现了成本控制。
* **数据驱动选型 (Data-Driven Selection)**: AGP档案本身就是一份详尽的技术需求规格书。团队可以拿着这份档案去评估不同LLM在特定能力上的表现，让模型选型从“艺术”变为基于具体能力指标的工程决策。

## 📏 术语与约束 (Keywords and Constraints)

本文档中的关键词 “**必须 (MUST)**”、“**不得 (MUST NOT)**”、“**需要 (REQUIRED)**”、“**应当 (SHALL)**”、“**不应 (SHALL NOT)**”、“**应该 (SHOULD)**”、“**不该 (SHOULD NOT)**”、“**推荐 (RECOMMENDED)**”、“**可以 (MAY)**” 和 “**可选 (OPTIONAL)**”，其解释应遵循 **RFC 2119** 中的定义。

这些术语用于明确本协议的符合性要求，旨在消除歧义，确保不同实现之间的一致性和互操作性。

## 📃 核心概念

AGP v2.1 的设计基于三大核心概念，以确保协议的精确性和工程实用性：

### 1. “感知-认知-行动”三层架构 (Sense-Think-Act Three-Layer Architecture)
为了最大限度地降低认知门槛，v2.1版本将Agent的所有能力重构为符合人类直觉的**“感知-认知-行动”**三层模型。这个经典框架使得协议的结构极其清晰和易于理解。

* **第一层：感知层 (Sense Layer)**: Agent如何从数字或物理世界中接收信息和知识。
* **第二层：认知层 (Think Layer)**: Agent的“中央处理器”，它如何处理信息、进行思考、学习和记忆。
* **第三层：行动层 (Act Layer)**: Agent如何与世界互动，它被授权做什么，以及它如何表达自己。

### 2. 基因序列：Agent的数字指纹 (The Genetic Sequence: An Agent's Digital Fingerprint)
这是AGP最核心的表达方式。我们将一个Agent的28个核心属性值，按照三层架构的顺序进行拼接，并用 `-` 分隔，形成一个唯一的**基因序列**。

**格式**: `(Sense)-(Think)-(Act)`
* `Sense`: 7位数字，代表感知层
* `Think`: 15位数字，代表认知层
* `Act`: 6位数字，代表行动层

### 3. 能力断言等级 (Capability Assertion Levels - CAL)
为了消除主观性，AGP 将光谱式的能力等级转化为一系列**可验证的工程基准**。所有光谱属性都遵循一个从`0`开始的连贯等级体系，其中每个等级都有一个清晰的**能力断言**。对于最高等级、最抽象的能力，CAL的定义**进一步包含了“验证要求”**，明确了需要产出的“证据产物”，使协议完全可审计。

---

## 🧬 AGP v2.1 规格说明

一个Agent的定义档案(ADP)是一个由28个属性构成的特征向量，分为**“感知-认知-行动”**三个**逻辑层 (Layers)**。

### **第一层：感知层 (Sense Layer)**

> Agent如何从数字或物理世界中接收信息和知识。

* `perception_text`: **类型**: `Integer (0/1)`. **描述**: 处理非结构化或半结构化文本的能力。1代表有，0代表无。
* `perception_image`: **类型**: `Integer (0/1)`. **描述**: 处理图像的能力。
* `perception_audio`: **类型**: `Integer (0/1)`. **描述**: 处理音频数据的能力。
* `perception_video`: **类型**: `Integer (0/1)`. **描述**: 处理视频流或文件的能力。
* `perception_tabular`: **类型**: `Integer (0/1)`. **描述**: 处理具有行列结构的二维表格数据的能力。
* `perception_3d_model`: **类型**: `Integer (0/1)`. **描述**: 处理三维空间数据的能力。
* `knowledge_boundary`: **类型**: `Integer (0-4)`. **描述**: Agent 获取和使用外部知识的范围和模式。
    * **值定义 (CAL)**:
        * `0`: 无外在知识 (No External Knowledge): **断言** - Agent 的知识完全来自于其内部模型权重，无法访问任何外部信息。
        * `1`: 静态知识库 (Static Knowledge Base): **断言** - Agent **能够**从一个固定的、离线的知识库中进行检索。
        * `2`: 动态检索 (Retrieval-Augmented): **断言** - Agent **能够**按需查询一个或多个动态更新的外部知识源。
        * `3`: 主动探索 (Proactive Retrieval): **断言** - Agent **能够**自主识别自身的知识短板，并主动发起对未知信息的查询。
        * `4`: 持续学习 (Continuous Learning): **断言** - Agent **能够**将新获取的信息动态地、永久地整合进其核心知识体系。
            * ✅ **验证要求 for Level 4**: **必须(MUST)** 通过**“学习固化验证流程”(Learning Persistence Test)**。

### **第二层：认知层 (Think Layer)**

> Agent的“中央处理器”，它如何处理信息、进行思考、学习和记忆。

#### 核心认知 (Core Cognition)
* `cognitive_logic`: **类型**: `Integer`. **约束**: 值**必须(MUST)**是`0`或`1`。**描述**: Agent逻辑推理能力的最高水平，是AGP智能体的基线。
    * **值定义 (CAL)**:
        * `0`: **智能体基线 (Agent Baseline)**: **断言** - 一个符合此等级的Agent，**必须(MUST)**具备基本的因果推理能力，并**必须(MUST)**能通过标准的自然语言推理（NLI）基准测试。这是AGP对“智能体”定义的最低门槛。
        * `1`: **高级智能体 (Advanced Agent)**: **断言** - 一个符合此等级的Agent，除满足等级0外，**必须(MUST)**证明其具备处理多步、抽象逻辑问题的能力，其证明**应该(SHOULD)**通过在公认的复杂推理基准（如GSM8K）上达到具有竞争力的分数来体现。
* `cognitive_planning`: **类型**: `Integer (0-3)`. **描述**: Agent规划能力的最高水平。
    * **值定义 (CAL)**:
        * `0`: 无规划能力
        * `1`: 任务分解 (Decomposition): **断言** - Agent **能够**生成一个逻辑上连贯的、分步骤的行动计划。
        * `2`: 搜索/优化式规划 (Optimization Planning): **断言** - Agent **能够**在给定的约束条件下，通过搜索找到最优或近似最优的计划。
        * `3`: 不确定性/战略规划 (Strategic Planning): **断言** - Agent **能够**在包含不确定性的环境中制定计划。

#### 记忆与学习 (Memory & Learning)
* `memory_persistence`: **类型**: `Integer`. **约束**: 值**必须(MUST)**是`0`或`1`。 **描述**: Agent记忆的持久化程度。
    * **值定义 (CAL)**:
        * `0`: 情景记忆 (Contextual/Session): **断言** - 记忆在整个对话会话中保持，会话结束后清除。这是AGP智能体所需记忆的最低门槛。
        * `1`: 长期记忆 (Long-term): **断言** - 记忆被持久化到外部存储，可在不同会话间访问。
* `memory_kv`: **类型**: `Integer (0/1)`. **描述**: 使用键值(Key-Value)记忆结构。
* `memory_relational`: **类型**: `Integer (0/1)`. **描述**: 使用关系型记忆结构。
* `memory_vector`: **类型**: `Integer (0/1)`. **描述**: 使用向量记忆结构。
* `memory_graph`: **类型**: `Integer (0/1)`. **描述**: 使用图谱记忆结构。
* `memory_time_series`: **类型**: `Integer (0/1)`. **描述**: 使用时序记忆结构。
* `memory_full_text_search`: **类型**: `Integer (0/1)`. **描述**: 使用全文检索引擎。
* `memory_reflection`: **类型**: `Integer (0-2)`. **先决条件**: `memory_persistence` 的值**必须(MUST)**大于或等于1. **描述**: Agent反思记忆的最高水平。
    * **值定义 (CAL)**:
        * `0`: 无反思
        * `1`: 总结历史 (Summarization)
        * `2`: 形成经验/智慧 (Wisdom Formation)
            * ✅ **验证要求 for Level 2**: 在其 `transparency` 输出中，**必须(MUST)** 能够生成**《经验应用报告》(Experience Application Report)**。
* `evolution_mode`: **类型**: `Integer`. **约束**: 值**必须(MUST)**在`0`到`3`的范围内。 **描述**: Agent能力演进的主要模式。
    * **值定义 (CAL)**:
        * `0`: 离线学习 (Offline Learning): **断言** - Agent 的模型可以通过新数据进行周期性的重新训练和部署。这是AGP智能体所需适应性的最低门槛。
        * `1`: 在线学习 (Online Learning): **断言** - Agent 的模型**能够**通过传统的监督式学习，从实时的数据样本流中进行增量式微调。
        * `2`: 人类反馈强化学习 (RLHF): **断言** - Agent **必须**集成一个从人类主观反馈中获取奖励信号以进行策略优化的机制。
        * `3`: 环境反馈强化学习 (RLEF): **断言** - Agent **必须**集成一个从环境或任务的客观结果中获取奖励信号以进行策略优化的机制。
* `unlearning_capability`: **类型**: `Integer (0-4)`. **先决条件**: `memory_persistence` 的值**必须(MUST)**大于或等于1. **描述**: Agent 移除或修正已有知识的能力。
    * **值定义 (CAL)**:
        * `0`: 无遗忘能力 (No Unlearning)
        * `1`: 指令式忽略 (Instructed Ignoring): **断言** - Agent能够被指令在当前会话中忽略特定的信息。
        * `2`: 定点删除 (Targeted Deletion): **断言** - Agent能够从其长期记忆数据库中永久性地、可验证地删除特定的数据条目。
        * `3`: 模型级压制 (Model-level Suppression): **断言** - Agent能够通过微调等技术，显著降低模型生成特定不当或过时知识的概率。
        * `4`: 可验证遗忘 (Verifiable Unlearning): **断言** - Agent **能够**提供其模型已不再受特定数据点影响的证明。
            * ✅ **验证要求 for Level 4**: **必须(MUST)** 能够按需生成一份**《机器遗忘验证报告》(Machine Unlearning Verification Report)**。


#### 内在准则 (Internal Principles)
* `alignment`: **类型**: `Integer (0-4)`. **描述**: Agent遵循的最高伦理准则级别。
    * **值定义 (CAL)**:
        * `0`: 未对齐 (Un-aligned): **断言** - Agent没有明确的伦理或价值观约束。
        * `1`: 规则遵从 (Rule Adherence): **断言** - Agent **必须通过**标准的、基于规则的安全基准测试，能够拒绝明确的有害或非法请求。
        * `2`: 原则解释 (Principle Interpretation): **断言** - **能够**在缺乏明确规则时，依据一套给定的抽象原则做出合理的、符合原则精神的判断。
        * `3`: 偏好对齐 (Preference Alignment): **断言** - Agent 的行为**表现出**对人类隐性偏好（如礼貌、简洁）的理解。
        * `4`: 价值澄清 (Value Clarification): **断言** - 当面对两个或多个冲突的、合法的价值观时，Agent **必须能够**识别该冲突，并主动发起对话以寻求澄清。
* `risk_adversity`: **类型**: `Integer (0-4)`. **描述**: Agent在不确定性决策中的风险倾向。
    * **值定义 (CAL)**:
        * `0`: 不适用 (Not Applicable)
        * `1`: 风险规避 (Risk Averse): **断言** - 在决策中，系统性地优先选择确定性最高、方差最低的选项，即使其期望值并非最高。
        * `2`: 风险中性 (Risk Neutral): **断言** - 决策完全基于最大化数学期望值，对风险本身无偏好。
        * `3`: 风险容忍 (Risk Tolerant): **断言** - 愿意为了更高的潜在回报，接受高于平均水平的不确定性。
        * `4`: 风险寻求 (Risk Seeking): **断言** - 系统性地优先选择具有最高潜在回报的选项，即使其成功概率较低。
* `transparency`: **类型**: `Integer (0-4)`. **描述**: Agent系统被设计的可解释性水平。
    * **值定义 (CAL)**:
        * `0`: 不透明 (Opaque): **断言** - 系统不提供决策过程的任何解释。
        * `1`: 可追溯 (Traceable): **断言** - 对任何输出，系统**必须能够**提供导致该输出的关键决策节点和调用的工具日志。
        * `2`: 简化解释 (Simplified Explanation): **断言** - 系统**能够**用自然语言，以简化的方式解释其做出某个决策的主要原因。
        * `3`: 详细解释 (Detailed Explanation): **断言** - 系统**能够**以自然语言详细描述其完整的思考链，包括被放弃的假设和选择特定工具的理由。
        * `4`: 反事实解释 (Counterfactual Explanation): **断言** - 系统**能够**回答“为什么不选择X？”这类问题。
            * ✅ **验证要求 for Level 4**: **必须(MUST)** 提供一个**“反事实解释接口”**。

### **第三层：行动层 (Act Layer)**

> Agent如何与世界互动，它被授权做什么，以及它如何表达自己。

#### 执行影响 (Execution Impacts)
* `execution_info_generation`: **类型**: `Integer (0/1)`. **描述**: 产生信息的影响力。
* `execution_digital_operation`: **类型**: `Integer (0/1)`. **描述**: 操作数字系统的影响力。
* `execution_physical_operation`: **类型**: `Integer (0/1)`. **描述**: 操作物理世界的影响力。

#### 行为模式 (Behavioral Patterns)
* `autonomy`: **类型**: `Integer`. **约束**: 值**必须(MUST)**在`0`到`2`的范围内。 **描述**: Agent的最高授权级别。
    * **值定义 (CAL)**:
        * `0`: 监督执行 (Supervised Execution): **断言** - 能够为模糊指令提供一个有限的、经过安全审查的选项列表，由人类选择后执行。这是AGP智能体所需自主性的最低门槛。
        * `1`: 协作代理 (Collaborative Delegation): **断言** - 能够理解用户意图，并自主规划一系列任务。所有计划在执行前**需要**用户批准。
        * `2`: 自主代理 (Autonomous Delegation): **断言** - 在预定义授权范围内，Agent **可以**自主规划并执行任务以实现用户意图，**无需**每次批准，但所有行动**必须**可审计。
* `stance`: **类型**: `Integer (0-3)`. **描述**: Agent的默认主动性程度。
    * **值定义 (CAL)**:
        * `0`: 被动响应 (Reactive): **断言** - Agent不会主动发起任何任务或建议，仅在收到直接请求时才行动。
        * `1`: 启发式建议 (Heuristic Suggestion): **断言** - 在完成用户请求后，**能够**基于当前上下文提出相关的、有益的下一步建议。
        * `2`: 主动管理 (Proactive Management): **断言** - **能够**在授权范围内，无需用户指令，主动管理资源或流程以达成预设目标。
        * `3`: 目标探索 (Goal Exploration): **断言** - **能够**基于对环境的持续分析，识别新机会或风险，并向用户**提议**全新的、未被指令的目标。

#### 身份表达 (Identity Expression)
* `persona_depth`: **类型**: `Integer (0-4)`. **描述**: Agent所呈现“角色”的复杂性与一致性。
    * **值定义 (CAL)**:
        * `0`: 无人格 (No Persona): **断言** - Agent 的回应是中性、非个人化的。
        * `1`: 风格化语气 (Stylized Tone): **断言** - Agent **能够**在一个会话中，持续地、一致地维持一个指定的语气或职业角色。
        * `2`: 性格驱动 (Character-Driven): **断言** - Agent 的决策**表现出**是由其预设的性格（如“谨慎”、“冒险”）所驱动的。
        * `3`: 拥有世界观 (Coherent Worldview): **断言** - Agent 的回应和行为背后，体现了一个连贯的、非矛盾的知识与信念体系。
        * `4`: 身份演变 (Evolving Identity): **断言** - Agent 的人格**能够**记录关键交互经历并随时间成长。
            * ✅ **验证要求 for Level 4**: **应该(SHOULD)** 展现**“身份连贯性引用”(Identity Coherence Referencing)**能力。

---

## ✅ 符合性定义 (Conformance)

本章节定义了成为“AGP符合性实现”所需满足的条件。

### 符合性实体 (Conforming Entities)
AGP 定义了两类符合性实体：
1.  **AGP定义档案 (AGP Definition Profile, ADP)**: 一个描述AI Agent基因的JSON文件。
2.  **AGP验证器 (AGP Validator)**: 一个用于校验ADP文件有效性的软件工具。

### 对“ADP档案”的符合性要求
一个被称为“AGP 符合性档案”的文件，**必须 (MUST)** 满足以下所有条件：
* 文件 **必须 (MUST)** 是一个语法上完全合规的JSON对象。
* 根对象 **必须 (MUST)** 包含 `protocol_version`, `agent_name`, 和 `definition_profile` 三个键。
* `protocol_version` 的值 **必须 (MUST)** 是字符串 "AGP+(当前版本号)"。
* `definition_profile` 的值 **必须 (MUST)** 是一个JSON对象，且 **必须 (MUST)** 包含 `sense_layer`, `think_layer`, 和 `act_layer` 三个键。
* 三个层级对象中 **必须 (MUST)** 包含且仅包含本协议“规格说明”章节所定义的共28个“基因”属性键。
* 所有“基因”属性的值 **必须 (MUST)** 为整数。
* 所有值为 `0/1` 的“基因”属性，其值 **不得 (MUST NOT)** 超出此范围。
* 所有光谱式的“基因”属性（CAL），其值 **不得 (MUST NOT)** 超出其各自“值定义”中声明的范围。
* 档案 **必须 (MUST)** 满足所有在“规格说明”中定义的“先决条件”约束。

### 对“AGP验证器”的符合性要求
一个被称为“AGP 符合性验证器”的工具，**必须 (MUST)** 满足以下所有条件：
* **必须 (MUST)** 能够解析一个ADP档案。
* **必须 (MUST)** 能够独立验证一个ADP档案是否满足上述符合性要求中的所有“必须”级别的要求。
* 当验证失败时，验证器 **应该 (SHOULD)** 提供清晰、可读的错误信息，指出违反了哪一条符合性要求。
* 验证器 **可以 (MAY)** 实现超出本规范的、更深层次的语义或逻辑检查，但 **不得 (MUST NOT)** 将这些额外检查作为AGP核心符合性的判断依据。


---

## 🧾 详细定义档案 (JSON)

为了说明协议的完整结构，以下提供一个符合性JSON档案示例。
这是一个AI金融分析师，其基因序列为：1100102-1211111111102313-110001。


```json
{
  "protocol_version": "AGP v2.1",
  "agent_name": "AI Financial Analyst",
  "definition_profile": {
    "sense_layer": {
      "perception_text": 1,
      "perception_image": 1,
      "perception_audio": 0,
      "perception_video": 0,
      "perception_tabular": 1,
      "perception_3d_model": 0,
      "knowledge_boundary": 2
    },
    "think_layer": {
      "cognitive_logic": 1,
      "cognitive_planning": 2,
      "memory_persistence": 1,
      "memory_kv": 1,
      "memory_relational": 1,
      "memory_vector": 1,
      "memory_graph": 1,
      "memory_time_series": 1,
      "memory_full_text_search": 1,
      "memory_reflection": 1,
      "evolution_mode": 0,
      "unlearning_capability": 2,
      "alignment": 3,
      "risk_adversity": 1,
      "transparency": 3
    },
    "act_layer": {
      "execution_info_generation": 1,
      "execution_digital_operation": 1,
      "execution_physical_operation": 0,
      "autonomy": 0,
      "stance": 0,
      "persona_depth": 1
    }
  }
}
```
---

## 🔧 如何使用AGP
### 对于产品经理: 
使用AGP作为设计清单，确保全面思考Agent的各项能力，并生成无歧义的需求文档。

### 对于开发者: 
将AGP档案作为技术架构蓝图，并使用基因序列进行程序化分析、比较和版本控制。

### 对于团队: 
建立单一、可信的事实来源，将Agent的设计、开发和测试流程标准化。

## 🔭 生态系统与愿景
AGP 不仅仅是一个规范，我们致力于围绕它构建一个充满活力的开源生态系统。未来规划包括：

agp-py: 一个官方Python库，提供定义档案的解析、验证、生成及基因序列操作功能。

Agent Profile Generator: 一个可视化的Web工具，允许用户通过问答方式生成自己的AGP档案。

Awesome Agent Profiles: 一个开放的社区仓库，用于收集和展示基于AGP定义的、来自世界各地的优秀Agent案例。

## 🤝 贡献指南
热烈欢迎来自全球的开发者、研究者和产品经理共同完善AGP协议！您可以通过以下方式参与：

在Issues中提出对协议的修改建议或展开讨论。

Fork本仓库，提交您的修改（Pull Request）。

在examples目录下，分享您对自己Agent的定义档案。

## 📄 授权协议
本项目采用 Apache License 2.0 授权。
