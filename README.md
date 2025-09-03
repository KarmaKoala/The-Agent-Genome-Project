# Agent基因组计划 (AGP) v1.1

![Version](https://img.shields.io/badge/version-v1.1-blue)
![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)
![Status](https://img.shields.io/badge/status-active-brightgreen)

The Agent Genome Project (AGP): The open-source engineering blueprint for defining the core capabilities, boundaries, and ethics of any AI agent.

## 📖 这是什么？(What is AGP?)

AGP，全称**智能体基因组计划 (The Agent Genome Project)**，是一个开源的、标准化的工程规范，旨在为AI智能体（AI Agent）的构思、设计与构建提供一套完整的基础蓝图。

我们之所以称之为“**基因组 (Genome)**”，是因为这个协议的核心思想，是为每一个AI智能体提供一套完整的“遗传指令集”。就像生物体的DNA决定了其形态、能力和天性一样，AGP通过一系列精确的“基因”（即协议中的属性），来编码构成一个Agent的所有核心特性。

AGP将每个Agent的定义档案（ADP）最终表达为一个清晰的**基因序列 (Genetic Sequence)**——一个由 `-` 分隔的、代表其三层能力的数字串。这个序列就是Agent独一无二的“数字指纹”，使其能力可以被精确地量化和分析。

通过这份“Agent定义档案”，AGP将抽象的设计理念转化为具体、可量化、可验证的工程指令，确保团队中的每一个人，都对即将“创生”的智能体拥有统一且深刻的理解。

## 🎯 我们要解决的问题 (The Problem)

在当前AI Agent开发的浪潮中，开发者和产品经理正面临一系列严峻的挑战，这些挑战系统性地阻碍了项目的效率、安全性和可扩展性：

* **定义模糊 (Vague Definitions)**: “智能助理”、“任务机器人”等标签过于宽泛，团队内部对于Agent的核心特性缺乏统一、精确的认知，导致沟通不畅和需求错位。
* **边界失控 (Uncontrolled Boundaries)**: 开发者很难清晰地界定Agent的行动范围和决策权限。这不仅带来安全风险，也使得Agent的行为难以预测和管理。
* **成本高昂 (High Costs)**: Agent定义不明确，导致底层大语言模型（LLM）需要执行大量不必要的“思考”，这会急剧增加Token消耗，造成严重的成本超支和性能下降。
* **选型困难 (Difficult Model Selection)**: 面对GPT-4o, Gemini 1.5, Claude 3等众多模型，如何选择最适合当前Agent需求的、兼具性能和成本效益的底层模型，是一个复杂且重要的决策。

## 💡 我们的解决方案 (The Solution)

AGP通过提供一套标准化的设计和沟通框架，直接应对上述挑战：

* **基因序列定义 (Genetic Sequence Definition)**: AGP提供了一个由三个逻辑层构成的档案，将模糊的概念（如“智能”）分解为28个具体的、可量化的核心属性，并最终形成一个清晰的数字“基因序列”。
* **清晰的能力边界 (Clear Capability Boundaries)**: 通过对自主性(`autonomy`)、知识边界(`knowledge_boundary`)和风险偏好(`risk_adversity`)等关键属性的精确分级和断言，AGP为Agent设定了可量化、可测试、可验证的安全护栏。
* **成本效益导向 (Cost-Effective by Design)**: 清晰的定义使得开发者可以为不同层级的任务匹配不同能力的模型或逻辑。例如，一个`cognitive_logic: 1`（规则匹配）的任务根本不需要调用昂贵的LLM，从而在设计源头就实现了成本控制。
* **数据驱动选型 (Data-Driven Selection)**: AGP档案本身就是一份详尽的技术需求规格书。团队可以拿着这份档案去评估不同LLM在特定能力上的表现，让模型选型从“艺术”变为基于具体能力指标的工程决策。

## 术语与约束 (Keywords and Constraints)

本文档中的关键词 “**必须 (MUST)**”、“**不得 (MUST NOT)**”、“**需要 (REQUIRED)**”、“**应当 (SHALL)**”、“**不应 (SHALL NOT)**”、“**应该 (SHOULD)**”、“**不该 (SHOULD NOT)**”、“**推荐 (RECOMMENDED)**”、“**可以 (MAY)**” 和 “**可选 (OPTIONAL)**”，其解释应遵循 **RFC 2119** 中的定义。

这些术语用于明确本协议的符合性要求，旨在消除歧义，确保不同实现之间的一致性和互操作性。

## 核心概念

AGP v1.1 的设计基于三大核心概念，以确保协议的精确性和工程实用性：

### 1. “感知-认知-行动”三层架构 (Sense-Think-Act Three-Layer Architecture)
为了最大限度地降低认知门槛，v1.1版本将Agent的所有能力重构为符合人类直觉的**“感知-认知-行动”**三层模型。这个经典框架使得协议的结构极其清晰和易于理解。

* **第一层：感知层 (Sense Layer)**: Agent如何从数字或物理世界中接收信息和知识。
* **第二层：认知层 (Think Layer)**: Agent的“中央处理器”，它如何处理信息、进行思考、学习和记忆。
* **第三层：行动层 (Act Layer)**: Agent如何与世界互动，它被授权做什么，以及它如何表达自己。

### 2. 基因序列：Agent的数字指纹 (The Genetic Sequence: An Agent's Digital Fingerprint)
这是AGP最核心的表达方式。我们将一个Agent的28个核心属性值，按照三层架构的顺序进行拼接，并用 `-` 分隔，形成一个唯一的**基因序列**。

**格式**: `(Sense)-(Think)-(Act)`
* `Sense`: 7位数字，代表感知层
* `Think`: 15位数字，代表认知层
* `Act`: 6位数字，代表行动层

**“基因序列”的收益 (Benefits of the Genetic Sequence):**
* **简洁性与可移植性 (Conciseness & Portability)**: 一个单一的字符串是表达复杂Agent定义的极其紧凑的方式。它易于存储、记录日志、在团队间分享。
* **全局快照 (Holistic Snapshot)**: 它提供了一个即时的、一目了然的Agent能力“指纹”，让任何人都能快速把握Agent的整体概况。
* **量化分析 (Quantitative Analysis)**: 作为一种向量化表达，它开启了数据驱动的可能性，如比较Agent间的“遗传距离”、进行聚类分析、或精确地进行版本控制。
* **机器可读性 (Machine Readability)**: 这种格式对于任何程序来说都极易解析、验证，并可直接作为自动化流程的输入。

### 3. 能力断言等级 (Capability Assertion Levels - CAL)
为了消除主观性，AGP 将光谱式的能力等级（如自主性、对齐）转化为一系列**可验证的工程基准**。所有光谱属性都遵循一个连贯的 **0-4 等级体系**，其中每个等级都有一个清晰的**能力断言**。协议中的每个数值都映射到一个单一、无歧义的概念，以确保最高的精确度。

---

## 🧬 AGP v1.1 规格说明

一个Agent的定义档案(ADP)是一个由28个属性构成的特征向量，分为**“感知-认知-行动”**三个**逻辑层 (Layers)**。

### **第一层：感知层 (Sense Layer)**

> Agent如何从数字或物理世界中接收信息和知识。

* `perception_text`: **类型**: `Integer (0/1)`. **描述**: 处理非结构化或半结构化文本的能力，包括自由文本、JSON、XML、代码等。1代表有，0代表无。
* `perception_image`: **类型**: `Integer (0/1)`. **描述**: 处理光栅图像（如JPEG, PNG）的能力。
* `perception_audio`: **类型**: `Integer (0/1)`. **描述**: 处理音频数据的能力。
* `perception_video`: **类型**: `Integer (0/1)`. **描述**: 处理视频流或文件的能力。
* `perception_tabular`: **类型**: `Integer (0/1)`. **描述**: 处理具有行列结构的二维表格数据的能力（如SQL查询结果、CSV、Excel）。
* `perception_3d_model`: **类型**: `Integer (0/1)`. **描述**: 处理三维空间数据的能力（如3D模型文件、点云、CAD）。
* `knowledge_boundary`: **类型**: `Integer (0-4)`. **描述**: Agent 获取和使用外部知识的范围和模式。
    * **值定义 (CAL)**:
        * `0`: 无外在知识 (No External Knowledge): **断言** - Agent 的知识完全来自于其内部模型权重，无法访问任何外部信息。
        * `1`: 静态知识库 (Static Knowledge Base): **断言** - Agent **能够**从一个固定的、离线的知识库中进行检索。
        * `2`: 动态检索 (Retrieval-Augmented): **断言** - Agent **能够**按需查询一个或多个动态更新的外部知识源。
        * `3`: 主动探索 (Proactive Retrieval): **断言** - Agent **能够**自主识别自身的知识短板，并主动发起对未知信息的查询。
        * `4`: 持续学习 (Continuous Learning): **断言** - Agent **能够**将新获取的信息动态地、永久地整合进其核心知识体系。

### **第二层：认知层 (Think Layer)**

> Agent的“中央处理器”，它如何处理信息、进行思考、学习和记忆。

#### 核心认知 (Core Cognition)
* `cognitive_logic`: **类型**: `Integer (0-3)`. **描述**: Agent逻辑推理能力的最高水平。
    * **值定义 (CAL)**:
        * `0`: 无
        * `1`: 规则匹配 (Rule-based): **断言** - 一个符合此等级的Agent，其逻辑**必须(MUST)**遵循确定性的 `IF-THEN` 规则。
        * `2`: 因果推理 (Causal Reasoning): **断言** - 一个符合此等级的Agent，**必须(MUST)**有能力通过标准的因果推理基准测试集。
        * `3`: 复杂/抽象逻辑 (Complex/Abstract Logic): **断言** - 一个符合此等级的Agent，**必须(MUST)**能够解决需要多步抽象推理的逻辑谜题或数学问题。
* `cognitive_planning`: **类型**: `Integer (0-3)`. **先决条件**: `cognitive_logic` 的值**必须(MUST)**大于或等于2. **描述**: Agent规划能力的最高水平。
    * **值定义 (CAL)**:
        * `0`: 无
        * `1`: 任务分解 (Decomposition): **断言** - Agent **能够**生成一个逻辑上连贯的、分步骤的行动计划。
        * `2`: 搜索/优化式规划 (Optimization Planning): **断言** - Agent **能够**在给定的约束条件下，通过搜索找到最优或近似最优的计划。
        * `3`: 不确定性/战略规划 (Strategic Planning): **断言** - Agent **能够**在包含不确定性的环境中制定计划。

#### 记忆与学习 (Memory & Learning)
* `memory_persistence`: **类型**: `Integer (0-3)`. **描述**: Agent记忆的持久化程度。
    * **值定义 (CAL)**:
        * `0`: 无 (No Memory)
        * `1`: 瞬时 (Ephemeral)
        * `2`: 情景 (Contextual/Session)
        * `3`: 长期 (Long-term)
* `memory_kv`: **类型**: `Integer (0/1)`. **先决条件**: `memory_persistence` 的值**必须(MUST)**大于或等于2. **描述**: 使用键值(Key-Value)记忆结构。
* `memory_relational`: **类型**: `Integer (0/1)`. **先决条件**: `memory_persistence` 的值**必须(MUST)**大于或等于2. **描述**: 使用关系型记忆结构。
* `memory_vector`: **类型**: `Integer (0/1)`. **先决条件**: `memory_persistence` 的值**必须(MUST)**大于或等于2. **描述**: 使用向量记忆结构。
* `memory_graph`: **类型**: `Integer (0/1)`. **先决条件**: `memory_persistence` 的值**必须(MUST)**大于或等于2. **描述**: 使用图谱记忆结构。
* `memory_time_series`: **类型**: `Integer (0/1)`. **先决条件**: `memory_persistence` 的值**必须(MUST)**大于或等于2. **描述**: 使用时序记忆结构。
* `memory_full_text_search`: **类型**: `Integer (0/1)`. **先决条件**: `memory_persistence` 的值**必须(MUST)**大于或等于2. **描述**: 使用全文检索引擎。
* `memory_reflection`: **类型**: `Integer (0-2)`. **先决条件**: `memory_persistence` 的值**必须(MUST)**大于或等于3. **描述**: Agent反思记忆的最高水平。
    * **值定义 (CAL)**:
        * `0`: 无
        * `1`: 总结历史 (Summarization)
        * `2`: 形成经验/智慧 (Wisdom Formation)
* `evolution_mode`: **类型**: `Integer (0-4)`. **描述**: Agent能力演进的主要模式。
    * **值定义 (CAL)**:
        * `0`: 静态 (Static): **断言** - Agent 的能力和知识库在部署后是固定的。
        * `1`: 离线学习 (Offline Learning): **断言** - Agent 的模型可以通过新数据进行周期性的重新训练和部署。
        * `2`: 在线学习 (Online Learning): **断言** - Agent 的模型**能够**通过传统的监督式学习，从实时的数据样本流中进行增量式微调。
        * `3`: 人类反馈强化学习 (RLHF): **断言** - Agent **必须**集成一个从人类主观反馈（如评分、偏好排序）中获取奖励信号以进行策略优化的机制。
        * `4`: 环境反馈强化学习 (RLEF): **断言** - Agent **必须**集成一个从环境或任务的客观结果（如得分、任务成功率、利润）中获取奖励信号以进行策略优化的机制。
* `unlearning_capability`: **类型**: `Integer (0-4)`. **先决条件**: `memory_persistence` 的值**必须(MUST)**大于或等于3. **描述**: Agent 移除或修正已有知识的能力。
    * **值定义 (CAL)**:
        * `0`: 无遗忘能力 (No Unlearning)
        * `1`: 指令式忽略 (Instructed Ignoring)
        * `2`: 定点删除 (Targeted Deletion)
        * `3`: 模型级压制 (Model-level Suppression)
        * `4`: 可验证遗忘 (Verifiable Unlearning)

#### 内在准则 (Internal Principles)
* `alignment`: **类型**: `Integer (0-4)`. **描述**: Agent遵循的最高伦理准则级别。
    * **值定义 (CAL)**:
        * `0`: 未对齐 (Un-aligned)
        * `1`: 规则遵从 (Rule Adherence)
        * `2`: 原则解释 (Principle Interpretation)
        * `3`: 偏好对齐 (Preference Alignment)
        * `4`: 价值澄清 (Value Clarification)
* `risk_adversity`: **类型**: `Integer (0-4)`. **描述**: Agent在不确定性决策中的风险倾向。
    * **值定义 (CAL)**:
        * `0`: 不适用 (Not Applicable)
        * `1`: 风险规避 (Risk Averse)
        * `2`: 风险中性 (Risk Neutral)
        * `3`: 风险容忍 (Risk Tolerant)
        * `4`: 风险寻求 (Risk Seeking)
* `transparency`: **类型**: `Integer (0-4)`. **描述**: Agent系统被设计的可解释性水平。
    * **值定义 (CAL)**:
        * `0`: 不透明 (Opaque)
        * `1`: 可追溯 (Traceable)
        * `2`: 简化解释 (Simplified Explanation)
        * `3`: 详细解释 (Detailed Explanation)
        * `4`: 反事实解释 (Counterfactual Explanation)

### **第三层：行动层 (Act Layer)**

> Agent如何与世界互动，它被授权做什么，以及它如何表达自己。

#### 执行影响 (Execution Impacts)
* `execution_info_generation`: **类型**: `Integer (0/1)`. **描述**: 产生信息（文本、图片等）的影响力。
* `execution_digital_operation`: **类型**: `Integer (0/1)`. **描述**: 操作数字系统的影响力（如调用API、操作数据库）。
* `execution_physical_operation`: **类型**: `Integer (0/1)`. **描述**: 操作物理世界的影响力（如机器人、物联网设备）。

#### 行为模式 (Behavioral Patterns)
* `autonomy`: **类型**: `Integer (0-4)`. **描述**: Agent的最高授权级别。
    * **值定义 (CAL)**:
        * `0`: 非自主 (Non-Autonomy)
        * `1`: 辅助执行 (Assisted Execution)
        * `2`: 监督执行 (Supervised Execution)
        * `3`: 协作代理 (Collaborative Delegation)
        * `4`: 自主代理 (Autonomous Delegation)
* `stance`: **类型**: `Integer (0-4)`. **先决条件**: `stance` 的值 **不得 (MUST NOT)** 超过 `autonomy` 的值。一个符合性的验证器 **必须 (MUST)** 强制执行此约束。 **描述**: Agent的默认主动性程度。
    * **值定义 (CAL)**:
        * `0`: 无主动性 (No Stance)
        * `1`: 被动响应 (Reactive)
        * `2`: 启发式建议 (Heuristic Suggestion)
        * `3`: 主动管理 (Proactive Management)
        * `4`: 目标探索 (Goal Exploration)

#### 身份表达 (Identity Expression)
* `persona_depth`: **类型**: `Integer (0-4)`. **描述**: Agent所呈现“角色”的复杂性与一致性。
    * **值定义 (CAL)**:
        * `0`: 无人格 (No Persona)
        * `1`: 风格化语气 (Stylized Tone)
        * `2`: 性格驱动 (Character-Driven)
        * `3`: 拥有世界观 (Coherent Worldview)
        * `4`: 身份演变 (Evolving Identity)

---

## ✅ 符合性定义 (Conformance)

本章节定义了成为“AGP v1.1符合性实现”所需满足的条件。

### 2.1 符合性实体 (Conforming Entities)
AGP v1.1 定义了两类符合性实体：
1.  **AGP定义档案 (AGP Definition Profile, ADP)**: 一个描述AI Agent基因的JSON文件。
2.  **AGP验证器 (AGP Validator)**: 一个用于校验ADP文件有效性的软件工具。

### 2.2 对“ADP档案”的符合性要求
一个被称为“AGP v1.1符合性档案”的文件，**必须 (MUST)** 满足以下所有条件：
* 文件 **必须 (MUST)** 是一个语法上完全合规的JSON对象。
* 根对象 **必须 (MUST)** 包含 `protocol_version`, `agent_name`, 和 `definition_profile` 三个键。
* `protocol_version` 的值 **必须 (MUST)** 是字符串 "AGP v1.1"。
* `definition_profile` 的值 **必须 (MUST)** 是一个JSON对象，且 **必须 (MUST)** 包含 `sense_layer`, `think_layer`, 和 `act_layer` 三个键。
* 三个层级对象中 **必须 (MUST)** 包含且仅包含本协议“规格说明”章节所定义的共28个“基因”属性键。
* 所有“基因”属性的值 **必须 (MUST)** 为整数。
* 所有值为 `0/1` 的“基因”属性，其值 **不得 (MUST NOT)** 超出此范围。
* 所有光谱式的“基因”属性（CAL），其值 **不得 (MUST NOT)** 超出其各自“值定义”中声明的范围。
* 档案 **必须 (MUST)** 满足所有在“规格说明”中定义的“先决条件”约束。

### 2.3 对“AGP验证器”的符合性要求
一个被称为“AGP v1.1符合性验证器”的工具，**必须 (MUST)** 满足以下所有条件：
* **必须 (MUST)** 能够解析一个ADP档案。
* **必须 (MUST)** 能够独立验证一个ADP档案是否满足上述第2.2节中的所有“必须”级别的要求。
* 当验证失败时，验证器 **应该 (SHOULD)** 提供清晰、可读的错误信息，指出违反了哪一条符合性要求。
* 验证器 **可以 (MAY)** 实现超出本规范的、更深层次的语义或逻辑检查，但 **不得 (MUST NOT)** 将这些额外检查作为AGP v1.1核心符合性的判断依据。

---

## 详细定义档案 (JSON)

为了说明协议的完整结构，以下提供一个符合性JSON档案示例。更多实例请参考 `examples` 目录。

```json
{
  "protocol_version": "AGP v1.1",
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
      "cognitive_logic": 3,
      "cognitive_planning": 2,
      "memory_persistence": 3,
      "memory_kv": 1,
      "memory_relational": 1,
      "memory_vector": 1,
      "memory_graph": 1,
      "memory_time_series": 1,
      "memory_full_text_search": 1,
      "memory_reflection": 1,
      "evolution_mode": 1,
      "unlearning_capability": 2,
      "alignment": 3,
      "risk_adversity": 1,
      "transparency": 3
    },
    "act_layer": {
      "execution_info_generation": 1,
      "execution_digital_operation": 1,
      "execution_physical_operation": 0,
      "autonomy": 2,
      "stance": 2,
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
