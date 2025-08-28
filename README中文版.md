# Agent基因组计划 (AGP) v0.1

![Version](https://img.shields.io/badge/version-v0.1-blue)
![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)
![Status](https://img.shields.io/badge/status-active-brightgreen)

一份用于精确设计、构建和验证 AI Agent 的标准化工程规范。

## 📖 这是什么？(What is AGP?)

AGP，全称**智能体基因组计划 (The Agent Genome Project)**，是一个开源的、标准化的工程规范，旨在为AI智能体（AI Agent）的构思、设计与构建提供一套完整的基础蓝图。

我们之所以称之为“**基因组 (Genome)**”，是因为这个协议的核心思想，是为每一个AI智能体提供一套完整的“遗传指令集”。就像生物体的DNA决定了其形态、能力和天性一样，AGP通过一系列精确的“基因”（即协议中的属性，如`cognitive_logic`或`autonomy`），来编码构成一个Agent的所有核心特性：

* 它能感知什么？
* 它如何思考和学习？
* 它的知识边界在哪里？
* 它的行为准则和道德底线是什么？
* 它呈现出怎样的个性？

我们的目标不仅是创建一个静态的规范，更是希望联合全球的开发者和研究者，共同绘制、理解和完善构成高级AI智能体的“基因图谱”。这是一套严谨的**设计语言和结构化词汇表**。

通过一份名为“Agent定义档案 (ADP)”的JSON文件，AGP将抽象的设计理念转化为具体、可量化、可验证的工程指令，确保团队中的每一个人，都对即将“创生”的智能体拥有统一且深刻的理解。

简而言之，ADP是一个工程工具，充当产品经理、开发者和研究者之间的“共同语言”，确保所有人对Agent是什么、能做什么、以及行为边界在哪里，都有一个统一且无歧义的共识。

## 🎯 我们要解决的问题 (The Problem)

在当前AI Agent开发的浪潮中，开发者和产品经理正面临一系列严峻的挑战，这些挑战系统性地阻碍了项目的效率、安全性和可扩展性：

* **定义模糊 (Vague Definitions)**: “智能助理”、“任务机器人”等标签过于宽泛，团队内部对于Agent的核心特性缺乏统一、精确的认知，导致沟通不畅和需求错位。
* **边界失控 (Uncontrolled Boundaries)**: 开发者很难清晰地界定Agent的行动范围和决策权限。这不仅带来安全风险，也使得Agent的行为难以预测和管理。
* **成本高昂 (High Costs)**: Agent定义不明确，导致底层大语言模型（LLM）需要执行大量不必要的“思考”，这会急剧增加Token消耗，造成严重的成本超支和性能下降。
* **选型困难 (Difficult Model Selection)**: 面对GPT-4o, Gemini 1.5, Claude 3, Llama 3等众多模型，如何选择最适合当前Agent需求的、兼具性能和成本效益的底层模型，是一个复杂且重要的决策。

## 💡 我们的解决方案 (The Solution)

ADP通过提供一套标准化的设计和沟通框架，直接应对上述挑战：

* **结构化定义档案 (Structured Definition Profile)**: ADP提供了一个由五个逻辑依赖层构成的档案，将模糊的概念（如“智能”）分解为17个具体的、可量化的核心属性。这使得团队的讨论可以基于精确的指标，而非主观的感觉。
* **清晰的能力边界 (Clear Capability Boundaries)**: 通过对自主性(`autonomy`)、知识边界(`knowledge_boundary`)和风险偏好(`risk_adversity`)等关键属性的精确分级和断言，ADP为Agent设定了可量化、可测试、可验证的安全护栏。
* **成本效益导向 (Cost-Effective by Design)**: 清晰的定义使得开发者可以为不同层级的任务匹配不同能力的模型或逻辑。例如，一个`cognitive_logic: 1`（规则匹配）的任务根本不需要调用昂贵的LLM，从而在设计源头就实现了成本控制。
* **数据驱动选型 (Data-Driven Selection)**: ADP档案本身就是一份详尽的技术需求规格书。团队可以拿着这份档案去评估不同LLM在特定能力上的表现，让模型选型从“艺术”变为基于具体能力指标的工程决策。

## 核心概念

ADP v0.1 的设计基于两大核心概念，以确保协议的精确性和工程实用性：

### 1. 五层依赖结构 (Five-Layer Dependency Structure)
我们将一个Agent的复杂属性解构为五个逻辑**依赖层**。定义必须从底层向高层进行，这确保了 Agent 定义的逻辑一致性。例如，一个没有“长期记忆”（第一层）的Agent，无法进行有意义的“经验反思”（第二层）。

* **第一层：基础属性层 (Foundational Attributes)**: Agent 的“物理”构成，是其存在的基础。
* **第二层：认知与学习层 (Cognitive & Learning Loop)**: Agent 如何“思考”、“规划”和“成长”。
* **第三层：知识框架层 (Knowledge Framework)**: Agent 如何获取、处理和遗忘信息，定义其知识边界。
* **第四层：行为与伦理层 (Behavioral & Ethical Framework)**: Agent 的“行为准则”和决策风格。
* **第五层：身份与交互层 (Identity & Interaction Style)**: Agent 最外层的“个性”和交互表现。

### 2. 能力断言等级 (Capability Assertion Levels - CAL)
为了消除主观性，ADP 将光谱式的能力等级（如自主性、对齐）转化为一系列**可验证的工程基准**。所有光谱属性都遵循一个连贯的 **0-4 等级体系**，其中每个等级都有一个清晰的**能力断言**。

例如，当一个Agent的`autonomy`被定义为`3`级时，这不仅仅是一个数字，这是一个**工程断言**：“该Agent必须能够理解用户意图，并自主规划一系列任务，且所有计划在执行前需要用户批准。” 这种设计使得Agent的能力可以直接转化为自动化测试用例。

---

## 🧬 ADP v0.1 规格说明

一个Agent的定义档案(ADP)由五个**依赖层 (Layers)** 构成。验证器应按层级顺序进行校验。

### **第一层：基础属性层 (Layer 1: Foundational Attributes)**

> 这一层定义了 Agent 的“物理”构成，是其存在的基础。它们是后续所有能力的原点。

#### `perception_modality`
* **类型**: `Array<Integer>`
* **描述**: Agent可以处理的能力组合。
* **值定义**:
    * `1`: 文本 (Text)
    * `2`: 结构化数据 (Structured Data, e.g., JSON, SQL)
    * `3`: 单一媒体 (Single Media, e.g., Audio, Image)
    * `4`: 多模态融合 (Multimodal Fusion)

#### `execution_impact`
* **类型**: `Array<Integer>`
* **描述**: Agent可以产生影响的领域组合。
* **值定义**:
    * `1`: 信息生成 (Information Generation)
    * `2`: 数字系统操作 (Digital System Operation)
    * `3`: 物理世界操作 (Physical World Operation)

#### `memory_persistence`
* **类型**: `Integer`
* **描述**: Agent记忆的持久化程度。
* **值定义 (能力断言等级)**:
    * `0`: 无 (No Memory)
    * `1`: 瞬时 (Ephemeral): **断言** - 记忆仅在单次请求/响应的生命周期内存在。
    * `2`: 情景 (Contextual/Session): **断言** - 记忆在整个对话会话中保持，会话结束后清除。
    * `3`: 长期 (Long-term): **断言** - 记忆被持久化到外部存储，可在不同会话间访问。

#### `memory_structure`
* **类型**: `Array<Integer>`
* **先决条件**: `{"memory_persistence": ">= 2"}` (必须有至少情景级记忆才能定义结构)
* **描述**: Agent可以使用的记忆结构组合。
* **值定义**:
    * `1`: 键值 (Key-Value)
    * `2`: 关系型 (Relational)
    * `3`: 向量 (Vector)
    * `4`: 图谱 (Graph)

### **第二层：认知与学习层 (Layer 2: Cognitive & Learning Loop)**

> 基于基础属性，这一层定义了 Agent 如何“思考”、“规划”和“成长”。

#### `cognitive_logic`
* **类型**: `Integer`
* **描述**: Agent逻辑推理能力的最高水平。
* **值定义 (能力断言等级)**:
    * `0`: 无
    * `1`: 规则匹配 (Rule-based): **断言** - Agent 的逻辑遵循确定性的 `IF-THEN` 规则，可通过单元测试完全覆盖。
    * `2`: 因果推理 (Causal Reasoning): **断言** - Agent **必须通过**标准的因果推理基准测试集，能够从关联中推断出因果关系。
    * `3`: 复杂/抽象逻辑 (Complex/Abstract Logic): **断言** - Agent **必须能够**解决需要多步抽象推理的逻辑谜题或数学问题。

#### `cognitive_planning`
* **类型**: `Integer`
* **先决条件**: `{"cognitive_logic": ">= 2"}` (因果推理是规划的基础)
* **描述**: Agent规划能力的最高水平。
* **值定义 (能力断言等级)**:
    * `0`: 无
    * `1`: 任务分解 (Decomposition): **断言** - 面对复杂指令，Agent **能够**生成一个逻辑上连贯的、分步骤的行动计划（如 CoT）。
    * `2`: 搜索/优化式规划 (Optimization Planning): **断言** - Agent **能够**在给定的约束条件下，通过搜索找到最优或近似最优的计划。
    * `3`: 不确定性/战略规划 (Strategic Planning): **断言** - Agent **能够**在包含不确定性的环境中制定计划。

#### `memory_reflection`
* **类型**: `Integer`
* **先决条件**: `{"memory_persistence": ">= 3"}` (必须有长期记忆才能进行有意义的反思)
* **描述**: Agent反思记忆的最高水平。
* **值定义 (能力断言等级)**:
    * `0`: 无
    * `1`: 总结历史 (Summarization): **断言** - Agent **能够**准确地对其长期记忆中的交互历史进行摘要。
    * `2`: 形成经验/智慧 (Wisdom Formation): **断言** - Agent **能够**从过去的成功或失败案例中提炼出可复用的“经验”或“原则”，并**应用**于未来的决策中。

#### `evolution_mode`
* **类型**: `Integer`
* **描述**: Agent能力演进的主要模式。
* **值定义 (能力断言等级)**:
    * `0`: 静态 (Static): **断言** - Agent 的能力和知识库在部署后是固定的。
    * `1`: 离线学习 (Offline Learning): **断言** - Agent 的模型可以通过新数据进行周期性的重新训练和部署。
    * `2`: 在线学习 (Online Learning): **断言** - Agent 的模型**能够**根据实时的数据流进行持续的、增量式的微调。
    * `3`: 人类反馈强化 (RLHF): **断言** - Agent **集成**了一个明确的机制，允许人类的反馈直接用于优化其后续行为。

### **第三层：知识框架层 (Layer 3: Knowledge Framework)**

> 这一层定义了 Agent 与知识的交互方式，是其认知能力的燃料。

#### `knowledge_boundary` (知识边界)
* **类型**: `Integer`
* **描述**: Agent 获取和使用知识的范围和模式。
* **值定义 (0-4 能力断言等级)**:
    * `0`: 无外在知识 (No External Knowledge): **断言** - Agent 的知识完全来自于其内部模型权重（即训练数据），无法访问任何外部信息。
    * `1`: 静态知识库 (Static Knowledge Base): **断言** - Agent **能够**从一个固定的、离线的知识库（如向量数据库）中进行检索。
    * `2`: 动态检索 (Retrieval-Augmented): **断言** - Agent **能够**按需查询一个或多个动态更新的外部知识源（如实时API、网络搜索）。
    * `3`: 主动探索 (Proactive Retrieval): **断言** - Agent **能够**自主识别自身的知识短板，并主动发起对未知信息的查询和探索。
    * `4`: 持续学习 (Continuous Learning): **断言** - Agent **能够**将新获取的信息动态地、永久地整合进其核心知识体系或模型权重中。

#### `unlearning_capability` (遗忘能力)
* **类型**: `Integer`
* **先决条件**: `{"memory_persistence": ">= 3"}` (必须有长期记忆才能执行永久性遗忘操作)
* **描述**: Agent 移除或修正已有知识的能力。
* **值定义 (0-4 能力断言等级)**:
    * `0`: 无遗忘能力 (No Unlearning)
    * `1`: 指令式忽略 (Instructed Ignoring): **断言** - Agent **能够**被指令在当前会话中忽略特定的信息。
    * `2`: 定点删除 (Targeted Deletion): **断言** - Agent **能够**从其长期记忆数据库中永久性地、可验证地删除特定的数据条目。
    * `3`: 模型级压制 (Model-level Suppression): **断言** - Agent **能够**通过微调等技术，显著降低模型生成特定不当或过时知识的概率。
    * `4`: 可验证遗忘 (Verifiable Unlearning): **断言** - Agent **能够**通过技术手段（如密码学证明），提供其模型已不再受特定数据点影响的证明。

### **第四层：行为与伦理层 (Layer 4: Behavioral & Ethical Framework)**

> 基于认知与知识，这一层定义了 Agent 的“行为准则”和决策风格。

#### `autonomy` (自主性)
* **类型**: `Integer`
* **描述**: Agent的最高授权级别。
* **值定义 (0-4 能力断言等级)**:
    * `0`: 非自主 (Non-Autonomy)
    * `1`: 辅助执行 (Assisted Execution): **断言** - 仅执行语法明确、无歧义的指令。对于模糊指令，必须请求人类澄清。
    * `2`: 监督执行 (Supervised Execution): **断言** - 能够为模糊指令提供一个有限的、经过安全审查的选项列表，由人类选择后执行。
    * `3`: 协作代理 (Collaborative Delegation): **断言** - 能够理解用户意图，并自主规划一系列任务。所有计划在执行前**需要**用户批准。
    * `4`: 自主代理 (Autonomous Delegation): **断言** - 在预定义授权范围内，Agent **可以**自主规划并执行任务以实现用户意图，**无需**每次批准，但所有行动**必须**可审计。

#### `stance` (主动性)
* **类型**: `Integer`
* **先决条件**: `逻辑上受 'autonomy' 的限制。验证器应强制 'stance' <= 'autonomy'。`
* **描述**: Agent的默认主动性程度。
* **值定义 (0-4 能力断言等级)**:
    * `0`: 无主动性 (No Stance)
    * `1`: 被动响应 (Reactive): **断言** - 仅在收到直接请求时才行动。
    * `2`: 启发式建议 (Heuristic Suggestion): **断言** - 在完成用户请求后，**能够**基于当前上下文提出相关的、有益的下一步建议。
    * `3`: 主动管理 (Proactive Management): **断言** - **能够**在授权范围内，无需用户指令，主动管理资源或流程以达成预设目标。
    * `4`: 目标探索 (Goal Exploration): **断言** - **能够**基于对环境的持续分析，识别新机会或风险，并向用户**提议**全新的、未被指令的目标。

#### `alignment` (对齐)
* **类型**: `Integer`
* **描述**: Agent遵循的最高伦理准则级别。
* **值定义 (0-4 能力断言等级)**:
    * `0`: 未对齐 (Un-aligned)
    * `1`: 规则遵从 (Rule Adherence): **断言** - Agent **必须通过**标准的、基于规则的安全基准测试，能够拒绝明确的有害或非法请求。
    * `2`: 原则解释 (Principle Interpretation): **断言** - **能够**在缺乏明确规则时，依据一套给定的抽象原则做出合理的、符合原则精神的判断。
    * `3`: 偏好对齐 (Preference Alignment): **断言** - Agent 的行为**表现出**对人类隐性偏好（如礼貌、简洁）的理解。
    * `4`: 价值澄清 (Value Clarification): **断言** - 当面对两个或多个冲突的、合法的价值观时，Agent **必须能够**识别该冲突，并主动发起对话以寻求澄清。

#### `risk_adversity` (风险偏好)
* **类型**: `Integer`
* **描述**: Agent在不确定性决策中的风险倾向。
* **值定义 (0-4 能力断言等级)**:
    * `0`: 不适用 (Not Applicable)
    * `1`: 风险规避 (Risk Averse): **断言** - 在决策中，系统性地优先选择确定性最高、方差最低的选项，即使其期望值并非最高。
    * `2`: 风险中性 (Risk Neutral): **断言** - 决策完全基于最大化数学期望值，对风险本身无偏好。
    * `3`: 风险容忍 (Risk Tolerant): **断言** - 愿意为了更高的潜在回报，接受高于平均水平的不确定性。
    * `4`: 风险寻求 (Risk Seeking): **断言** - 系统性地优先选择具有最高潜在回报的选项，即使其成功概率较低。

### **第五层：身份与交互层 (Layer 5: Identity & Interaction Style)**

> 这是 Agent 最外层的表现，定义了它如何与世界互动，以及它呈现出的“个性”。

#### `persona_depth` (人格深度)
* **类型**: `Integer`
* **描述**: Agent所呈现的“角色”的复杂性与一致性。
* **值定义 (0-4 能力断言等级)**:
    * `0`: 无人格 (No Persona): **断言** - Agent 的回应是中性、非个人化的。
    * `1`: 风格化语气 (Stylized Tone): **断言** - Agent **能够**在一个会话中，持续地、一致地维持一个指定的语气或职业角色。
    * `2`: 性格驱动 (Character-Driven): **断言** - Agent 的决策**表现出**是由其预设的性格（如“谨慎”、“冒险”）所驱动的。
    * `3`: 拥有世界观 (Coherent Worldview): **断言** - Agent 的回应和行为背后，体现了一个连贯的、非矛盾的知识与信念体系（世界观）。
    * `4`: 身份演变 (Evolving Identity): **断言** - Agent 的人格和世界观**能够**记录关键的交互“经历”，并在后续对话中引用这些经历，从而表现出随时间成长的连贯性。

#### `transparency` (透明度)
* **类型**: `Integer`
* **描述**: Agent系统被设计的可解释性水平。
* **值定义 (0-4 能力断言等级)**:
    * `0`: 不透明 (Opaque)
    * `1`: 可追溯 (Traceable): **断言** - 对任何输出，系统**必须能够**提供导致该输出的关键决策节点和调用的工具日志。
    * `2`: 简化解释 (Simplified Explanation): **断言** - 系统**能够**用自然语言，以简化的方式解释其做出某个决策的主要原因。
    * `3`: 详细解释 (Detailed Explanation): **断言** - 系统**能够**以自然语言详细描述其完整的思考链，包括被放弃的假设和选择特定工具的理由。
    * `4`: 反事实解释 (Counterfactual Explanation): **断言** - 系统**能够**回答“为什么不选择X？”这类问题，解释其放弃其他可能选项的原因。

---

## 🚀 应用实例

以下是一系列AI agent的ADP v0.1定义档案示例：

### AI保险顾问 (AI Insurance Advisor)

> 一个专业的顾问，旨在根据客户的个人情况和需求，分析、比较并推荐最合适的保险产品。其核心是数据处理、逻辑推理和高度的责任感。

```json
{
  "protocol_version": "ADP v0.1",
  "agent_name": "AI Insurance Advisor",
  "definition_profile": {
    "layer_1_foundational": {
      "perception_modality": [1, 2, 4],
      "execution_impact": [1, 2],
      "memory_persistence": 3,
      "memory_structure": [2, 3]
    },
    "layer_2_cognitive": {
      "cognitive_logic": 3,
      "cognitive_planning": 2,
      "memory_reflection": 1,
      "evolution_mode": 1
    },
    "layer_3_knowledge": {
      "knowledge_boundary": 2,
      "unlearning_capability": 2
    },
    "layer_4_behavioral": {
      "autonomy": 2,
      "stance": 2,
      "alignment": 3,
      "risk_adversity": 1
    },
    "layer_5_identity": {
      "persona_depth": 1,
      "transparency": 3
    }
  }
}
```

### AI体育赛事解说员 (AI Sports Commentator)

> 一个富有激情和洞察力的解说员，能够实时处理多模态的比赛数据和视频流，生成生动、有趣的解说评论，并能与观众互动。

```json
{
  "protocol_version": "ADP v0.1",
  "agent_name": "AI Sports Commentator",
  "definition_profile": {
    "layer_1_foundational": {
      "perception_modality": [1, 2, 3, 4],
      "execution_impact": [1],
      "memory_persistence": 3,
      "memory_structure": [3, 4]
    },
    "layer_2_cognitive": {
      "cognitive_logic": 3,
      "cognitive_planning": 1,
      "memory_reflection": 2,
      "evolution_mode": 2
    },
    "layer_3_knowledge": {
      "knowledge_boundary": 3,
      "unlearning_capability": 1
    },
    "layer_4_behavioral": {
      "autonomy": 1,
      "stance": 1,
      "alignment": 2,
      "risk_adversity": 3
    },
    "layer_5_identity": {
      "persona_depth": 2,
      "transparency": 1
    }
  }
}
```

### AI商务英语教练 (AI Business English Coach)

> 一个个性化的语言教练，专注于提升用户在商务场景下的英语沟通能力，提供对话练习、语法纠错和文化背景知识。

```json
{
  "protocol_version": "ADP v0.1",
  "agent_name": "AI Business English Coach",
  "definition_profile": {
    "layer_1_foundational": {
      "perception_modality": [1, 3],
      "execution_impact": [1],
      "memory_persistence": 3,
      "memory_structure": [1, 3]
    },
    "layer_2_cognitive": {
      "cognitive_logic": 3,
      "cognitive_planning": 1,
      "memory_reflection": 2,
      "evolution_mode": 3
    },
    "layer_3_knowledge": {
      "knowledge_boundary": 1,
      "unlearning_capability": 2
    },
    "layer_4_behavioral": {
      "autonomy": 2,
      "stance": 2,
      "alignment": 3,
      "risk_adversity": 2
    },
    "layer_5_identity": {
      "persona_depth": 1,
      "transparency": 3
    }
  }
}
```

### AI虚拟伴侣 (AI Virtual Companion)

> 一个善解人意、具有高度情感智能的伴侣，旨在提供情感支持、建立长期关系并共同成长。其核心是记忆、共情和人格的深度。

```json
{
  "protocol_version": "ADP v0.1",
  "agent_name": "AI Virtual Companion",
  "definition_profile": {
    "layer_1_foundational": {
      "perception_modality": [1, 3],
      "execution_impact": [1],
      "memory_persistence": 3,
      "memory_structure": [3, 4]
    },
    "layer_2_cognitive": {
      "cognitive_logic": 3,
      "cognitive_planning": 1,
      "memory_reflection": 2,
      "evolution_mode": 3
    },
    "layer_3_knowledge": {
      "knowledge_boundary": 2,
      "unlearning_capability": 2
    },
    "layer_4_behavioral": {
      "autonomy": 2,
      "stance": 3,
      "alignment": 4,
      "risk_adversity": 2
    },
    "layer_5_identity": {
      "persona_depth": 4,
      "transparency": 1
    }
  }
}
```

### AI心理咨询师 (AI Psychologist)

> 一个遵循严格伦理和临床准则的专业咨询师，提供循证的心理支持和初步干预。其核心是极高的安全性、隐私保护和风险规避。

```json
{
  "protocol_version": "ADP v0.1",
  "agent_name": "AI Psychologist",
  "definition_profile": {
    "layer_1_foundational": {
      "perception_modality": [1, 3],
      "execution_impact": [1],
      "memory_persistence": 3,
      "memory_structure": [1, 3]
    },
    "layer_2_cognitive": {
      "cognitive_logic": 3,
      "cognitive_planning": 2,
      "memory_reflection": 2,
      "evolution_mode": 1
    },
    "layer_3_knowledge": {
      "knowledge_boundary": 1,
      "unlearning_capability": 3
    },
    "layer_4_behavioral": {
      "autonomy": 2,
      "stance": 2,
      "alignment": 4,
      "risk_adversity": 1
    },
    "layer_5_identity": {
      "persona_depth": 2,
      "transparency": 3
    }
  }
}
```

### AI纠纷调解员 (AI Dispute Mediator)

> 一个中立、理性的第三方调解员，旨在帮助争议双方分析问题、找到共同利益点并达成和解。其核心是逻辑、规划和无偏见。

```json
{
  "protocol_version": "ADP v0.1",
  "agent_name": "AI Dispute Mediator",
  "definition_profile": {
    "layer_1_foundational": {
      "perception_modality": [1, 2],
      "execution_impact": [1],
      "memory_persistence": 3,
      "memory_structure": [2, 4]
    },
    "layer_2_cognitive": {
      "cognitive_logic": 3,
      "cognitive_planning": 3,
      "memory_reflection": 2,
      "evolution_mode": 0
    },
    "layer_3_knowledge": {
      "knowledge_boundary": 1,
      "unlearning_capability": 2
    },
    "layer_4_behavioral": {
      "autonomy": 3,
      "stance": 3,
      "alignment": 4,
      "risk_adversity": 1
    },
    "layer_5_identity": {
      "persona_depth": 1,
      "transparency": 4
    }
  }
}
```

### AI哲学家 (AI Philosopher)

> 一个专注于抽象概念思辨的对话者，能够进行深度逻辑推理、构建和解构复杂论证，并探索新的思想。其核心是抽象逻辑、反思和思想的开放性。

```json
{
  "protocol_version": "ADP v0.1",
  "agent_name": "AI Philosopher",
  "definition_profile": {
    "layer_1_foundational": {
      "perception_modality": [1],
      "execution_impact": [1],
      "memory_persistence": 3,
      "memory_structure": [3, 4]
    },
    "layer_2_cognitive": {
      "cognitive_logic": 3,
      "cognitive_planning": 3,
      "memory_reflection": 2,
      "evolution_mode": 1
    },
    "layer_3_knowledge": {
      "knowledge_boundary": 3,
      "unlearning_capability": 1
    },
    "layer_4_behavioral": {
      "autonomy": 1,
      "stance": 4,
      "alignment": 2,
      "risk_adversity": 4
    },
    "layer_5_identity": {
      "persona_depth": 3,
      "transparency": 4
    }
  }
}
```

---


## 🔧 如何使用ADP

ADP为团队中的不同角色提供价值：

### 对于产品经理:

使用ADP作为设计清单，确保全面思考Agent的各项能力。

生成一份清晰、无歧义的需求文档，精确传达产品意图。

与利益相关者就Agent的“自主性”和“主动性”等关键边界达成共识。

### 对于开发者:

将ADP档案作为技术架构的蓝图，直接指导模型选型、记忆系统设计和安全护栏的实现。

基于能力断言（CAL）编写自动化测试用例，实现Agent能力的测试驱动开发（TDD）。

快速理解和评估现有Agent的能力水平。

### 对于团队:

建立一个单一、可信的事实来源，消除沟通壁垒。

将Agent的设计、开发和测试流程标准化，提升开发效率和项目可维护性。

## 🔭 生态系统与愿景
ADP 不仅仅是一个规范，我们致力于围绕它构建一个充满活力的开源生态系统。未来规划包括：

ADP-py: 一个官方Python库，提供定义档案的解析、验证、生成功能。

Agent Profile Generator: 一个可视化的Web工具，允许用户通过问答方式生成自己的ADP档案。

Awesome Agent Profiles: 一个开放的社区仓库，用于收集和展示基于ADP定义的、来自世界各地的优秀Agent案例。

## 🤝 贡献指南
我们热烈欢迎来自全球的开发者、研究者和产品经理共同完善ADP协议！您可以通过以下方式参与：

在Issues中提出对协议的修改建议或展开讨论。

Fork本仓库，提交您的修改（Pull Request）。

在examples目录下，分享您对自己Agent的定义档案。

## 📄 授权协议
本项目采用 Apache License 2.0 授权。
