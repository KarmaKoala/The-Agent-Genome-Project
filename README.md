# Agent基因组计划 (AGP) v0.5

![Version](https://img.shields.io/badge/version-v0.5-blue)
![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)
![Status](https://img.shields.io/badge/status-active-brightgreen)

The Agent Genome Project (AGP): The open-source engineering blueprint for defining the core capabilities, boundaries, and ethics of any AI agent.

## 📖 这是什么？(What is AGP?)

AGP，全称**智能体基因组计划 (The Agent Genome Project)**，是一个开源的、标准化的工程规范，旨在为AI智能体（AI Agent）的构思、设计与构建提供一套完整的基础蓝图。

我们之所以称之为“**基因组 (Genome)**”，是因为这个协议的核心思想，是为每一个AI智能体提供一套完整的“遗传指令集”。就像生物体的DNA决定了其形态、能力和天性一样，AGP通过一系列精确的“基因”（即协议中的属性），来编码构成一个Agent的所有核心特性。

AGP将每个Agent的定义档案（ADP）最终表达为一个清晰的**基因序列 (Genetic Sequence)**——一个由 `-` 分隔的、代表其五层能力的数字串。这个序列就是Agent独一-无二的“数字指纹”，使其能力可以被精确地量化和分析。

通过这份“Agent定义档案”，AGP将抽象的设计理念转化为具体、可量化、可验证的工程指令，确保团队中的每一个人，都对即将“创生”的智能体拥有统一且深刻的理解。

## 🎯 我们要解决的问题 (The Problem)

在当前AI Agent开发的浪潮中，开发者和产品经理正面临一系列严峻的挑战，这些挑战系统性地阻碍了项目的效率、安全性和可扩展性：

* **定义模糊 (Vague Definitions)**: “智能助理”、“任务机器人”等标签过于宽泛，团队内部对于Agent的核心特性缺乏统一、精确的认知，导致沟通不畅和需求错位。
* **边界失控 (Uncontrolled Boundaries)**: 开发者很难清晰地界定Agent的行动范围和决策权限。这不仅带来安全风险，也使得Agent的行为难以预测和管理。
* **成本高昂 (High Costs)**: Agent定义不明确，导致底层大语言模型（LLM）需要执行大量不必要的“思考”，这会急剧增加Token消耗，造成严重的成本超支和性能下降。
* **选型困难 (Difficult Model Selection)**: 面对GPT-4o, Gemini 1.5, Claude 3, Llama 3等众多模型，如何选择最适合当前Agent需求的、兼具性能和成本效益的底层模型，是一个复杂且重要的决策。

## 💡 我们的解决方案 (The Solution)

AGP通过提供一套标准化的设计和沟通框架，直接应对上述挑战：

* **基因序列定义 (Genetic Sequence Definition)**: AGP提供了一个由五个逻辑依赖层构成的档案，将模糊的概念（如“智能”）分解为26个具体的、可量化的核心属性，并最终形成一个清晰的数字“基因序列”。
* **清晰的能力边界 (Clear Capability Boundaries)**: 通过对自主性(`autonomy`)、知识边界(`knowledge_boundary`)和风险偏好(`risk_adversity`)等关键属性的精确分级和断言，AGP为Agent设定了可量化、可测试、可验证的安全护栏。
* **成本效益导向 (Cost-Effective by Design)**: 清晰的定义使得开发者可以为不同层级的任务匹配不同能力的模型或逻辑。例如，一个`cognitive_logic: 1`（规则匹配）的任务根本不需要调用昂贵的LLM，从而在设计源头就实现了成本控制。
* **数据驱动选型 (Data-Driven Selection)**: AGP档案本身就是一份详尽的技术需求规格书。团队可以拿着这份档案去评估不同LLM在特定能力上的表现，让模型选型从“艺术”变为基于具体能力指标的工程决策。

## 📃 核心概念

AGP v0.5 的设计基于三大核心概念，以确保协议的精确性和工程实用性：

### 1. 基因序列：Agent的数字指纹 (The Genetic Sequence: An Agent's Digital Fingerprint)
这是AGP最核心的表达方式。我们将一个Agent的26个核心属性值，按照五层依赖结构的顺序进行拼接，并用 `-` 分隔，形成一个唯一的**基因序列**。

**格式**: `(L1)-(L2)-(L3)-(L4)-(L5)`
* `L1`: 14位数字，代表基础属性层
* `L2`: 4位数字，代表认知与学习层
* `L3`: 2位数字，代表知识框架层
* `L4`: 4位数字，代表行为与伦理层
* `L5`: 2位数字，代表身份与交互层

**“基因序列”的收益 (Benefits of the Genetic Sequence):**
* **简洁性与可移植性 (Conciseness & Portability)**: 一个单一的字符串是表达复杂Agent定义的极其紧凑的方式。它易于存储、记录日志、在团队间分享，甚至可以作为文件名或数据库主键。
* **全局快照 (Holistic Snapshot)**: 它提供了一个即时的、一目了然的Agent能力“指纹”，让任何人都能快速把握Agent的整体概况。
* **量化分析 (Quantitative Analysis)**: 作为一种向量化表达，它开启了数据驱动的可能性：
    * **比较**: 计算两个Agent之间的“遗传距离”（如汉明距离），以判断其能力相似性。
    * **聚类**: 对大量Agent进行聚类分析，发现其能力分布和典型“物种”。
    * **版本控制**: 通过对比序列差异，可以精确地看到Agent版本迭代中哪个“基因”发生了改变。
* **机器可读性 (Machine Readability)**: 这种格式对于任何程序来说都极易解析、验证，并可直接作为自动化流程的输入。

### 2. 五层依赖结构 (Five-Layer Dependency Structure)
我们将一个Agent的复杂属性解构为五个逻辑**依赖层**。定义必须从底层向高层进行，这确保了 Agent 定义的逻辑一致性。

* **第一层：基础属性层 (Foundational Attributes)**
* **第二层：认知与学习层 (Cognitive & Learning Loop)**
* **第三层：知识框架层 (Knowledge Framework)**
* **第四层：行为与伦理层 (Behavioral & Ethical Framework)**
* **第五层：身份与交互层 (Identity & Interaction Style)**

### 3. 能力断言等级 (Capability Assertion Levels - CAL)
为了消除主观性，AGP 将光谱式的能力等级（如自主性、对齐）转化为一系列**可验证的工程基准**。所有光谱属性都遵循一个连贯的 **0-4 等级体系**，其中每个等级都有一个清晰的**能力断言**。协议中的每个数值都映射到一个单一、无歧义的概念，以确保最高的精确度。

---

## 🧬 AGP v0.5 规格说明

一个Agent的定义档案(ADP)是一个由26个属性构成的特征向量，分为五个**依赖层 (Layers)**。

### **第一层：基础属性层 (Layer 1: Foundational Attributes)**

> 这一层定义了 Agent 的“物理”构成，是其存在的基础。

#### 感知模态 (Perception Modalities)
* `perception_text`: **类型**: `Integer (0/1)`. **描述**: 处理非结构化或半结构化文本的能力，包括自由文本、JSON、XML、代码等。1代表有，0代表无。
* `perception_image`: **类型**: `Integer (0/1)`. **描述**: 处理光栅图像（如JPEG, PNG）的能力。
* `perception_audio`: **类型**: `Integer (0/1)`. **描述**: 处理音频数据的能力。
* `perception_video`: **类型**: `Integer (0/1)`. **描述**: 处理视频流或文件的能力。
* `perception_tabular`: **类型**: `Integer (0/1)`. **描述**: 处理具有行列结构的二维表格数据的能力（如SQL查询结果、CSV、Excel）。
* `perception_3d_model`: **类型**: `Integer (0/1)`. **描述**: 处理三维空间数据的能力（如3D模型文件、点云、CAD）。

#### 执行影响 (Execution Impacts)
* `execution_info_generation`: **类型**: `Integer (0/1)`. **描述**: 产生信息（文本、图片等）的影响力。
* `execution_digital_operation`: **类型**: `Integer (0/1)`. **描述**: 操作数字系统的影响力（如调用API、操作数据库）。
* `execution_physical_operation`: **类型**: `Integer (0/1)`. **描述**: 操作物理世界的影响力（如机器人、物联网设备）。

#### `memory_persistence` (记忆持久化)
* **类型**: `Integer (0-3)`
* **描述**: Agent记忆的持久化程度。
* **值定义 (能力断言等级)**:
    * `0`: 无 (No Memory)
    * `1`: 瞬时 (Ephemeral): **断言** - 记忆仅在单次请求/响应的生命周期内存在。
    * `2`: 情景 (Contextual/Session): **断言** - 记忆在整个对话会话中保持，会话结束后清除。
    * `3`: 长期 (Long-term): **断言** - 记忆被持久化到外部存储，可在不同会话间访问。

#### 记忆结构 (Memory Structures)
* **先决条件**: `{"memory_persistence": ">= 2"}`
* `memory_kv`: **类型**: `Integer (0/1)`. **描述**: 使用键值(Key-Value)记忆结构。
* `memory_relational`: **类型**: `Integer (0/1)`. **描述**: 使用关系型记忆结构。
* `memory_vector`: **类型**: `Integer (0/1)`. **描述**: 使用向量记忆结构。
* `memory_graph`: **类型**: `Integer (0/1)`. **描述**: 使用图谱记忆结构。

### **第二层：认知与学习层 (Layer 2: Cognitive & Learning Loop)**

> 基于基础属性，这一层定义了 Agent 如何“思考”、“规划”和“成长”。

#### `cognitive_logic` (认知逻辑)
* **类型**: `Integer (0-3)`
* **描述**: Agent逻辑推理能力的最高水平。
* **值定义 (能力断言等级)**:
    * `0`: 无
    * `1`: 规则匹配 (Rule-based): **断言** - Agent 的逻辑遵循确定性的 `IF-THEN` 规则，可通过单元测试完全覆盖。
    * `2`: 因果推理 (Causal Reasoning): **断言** - Agent **必须通过**标准的因果推理基准测试集，能够从关联中推断出因果关系。
    * `3`: 复杂/抽象逻辑 (Complex/Abstract Logic): **断言** - Agent **必须能够**解决需要多步抽象推理的逻辑谜题或数学问题。

#### `cognitive_planning` (认知规划)
* **类型**: `Integer (0-3)`
* **先决条件**: `{"cognitive_logic": ">= 2"}`
* **描述**: Agent规划能力的最高水平。
* **值定义 (能力断言等级)**:
    * `0`: 无
    * `1`: 任务分解 (Decomposition): **断言** - 面对复杂指令，Agent **能够**生成一个逻辑上连贯的、分步骤的行动计划（如 CoT）。
    * `2`: 搜索/优化式规划 (Optimization Planning): **断言** - Agent **能够**在给定的约束条件下，通过搜索找到最优或近似最优的计划。
    * `3`: 不确定性/战略规划 (Strategic Planning): **断言** - Agent **能够**在包含不确定性的环境中制定计划。

#### `memory_reflection` (记忆反思)
* **类型**: `Integer (0-2)`
* **先决条件**: `{"memory_persistence": ">= 3"}`
* **描述**: Agent反思记忆的最高水平。
* **值定义 (能力断言等级)**:
    * `0`: 无
    * `1`: 总结历史 (Summarization): **断言** - Agent **能够**准确地对其长期记忆中的交互历史进行摘要。
    * `2`: 形成经验/智慧 (Wisdom Formation): **断言** - Agent **能够**从过去的成功或失败案例中提炼出可复用的“经验”或“原则”，并**应用**于未来的决策中。

#### `evolution_mode` (演进模式)
* **类型**: `Integer (0-3)`
* **描述**: Agent能力演进的主要模式。
* **值定义 (能力断言等级)**:
    * `0`: 静态 (Static): **断言** - Agent 的能力和知识库在部署后是固定的。
    * `1`: 离线学习 (Offline Learning): **断言** - Agent 的模型可以通过新数据进行周期性的重新训练和部署。
    * `2`: 在线学习 (Online Learning): **断言** - Agent 的模型**能够**根据实时的数据流进行持续的、增量式的微调。
    * `3`: 人类反馈强化 (RLHF): **断言** - Agent **集成**了一个明确的机制，允许人类的反馈直接用于优化其后续行为。

### **第三层：知识框架层 (Layer 3: Knowledge Framework)**

> 这一层定义了 Agent 与知识的交互方式，是其认知能力的燃料。

#### `knowledge_boundary` (知识边界)
* **类型**: `Integer (0-4)`
* **描述**: Agent 获取和使用知识的范围和模式。
* **值定义 (能力断言等级)**:
    * `0`: 无外在知识 (No External Knowledge): **断言** - Agent 的知识完全来自于其内部模型权重，无法访问任何外部信息。
    * `1`: 静态知识库 (Static Knowledge Base): **断言** - Agent **能够**从一个固定的、离线的知识库（如向量数据库）中进行检索。
    * `2`: 动态检索 (Retrieval-Augmented): **断言** - Agent **能够**按需查询一个或多个动态更新的外部知识源（如实时API、网络搜索）。
    * `3`: 主动探索 (Proactive Retrieval): **断言** - Agent **能够**自主识别自身的知识短板，并主动发起对未知信息的查询和探索。
    * `4`: 持续学习 (Continuous Learning): **断言** - Agent **能够**将新获取的信息动态地、永久地整合进其核心知识体系或模型权重中。

#### `unlearning_capability` (遗忘能力)
* **类型**: `Integer (0-4)`
* **先决条件**: `{"memory_persistence": ">= 3"}`
* **描述**: Agent 移除或修正已有知识的能力。
* **值定义 (能力断言等级)**:
    * `0`: 无遗忘能力 (No Unlearning)
    * `1`: 指令式忽略 (Instructed Ignoring): **断言** - Agent **能够**被指令在当前会话中忽略特定的信息。
    * `2`: 定点删除 (Targeted Deletion): **断言** - Agent **能够**从其长期记忆数据库中永久性地、可验证地删除特定的数据条目。
    * `3`: 模型级压制 (Model-level Suppression): **断言** - Agent **能够**通过微调等技术，显著降低模型生成特定不当或过时知识的概率。
    * `4`: 可验证遗忘 (Verifiable Unlearning): **断言** - Agent **能够**通过技术手段，提供其模型已不再受特定数据点影响的证明。

### **第四层：行为与伦理层 (Layer 4: Behavioral & Ethical Framework)**

> 基于认知与知识，这一层定义了 Agent 的“行为准则”和决策风格。

#### `autonomy` (自主性)
* **类型**: `Integer (0-4)`
* **描述**: Agent的最高授权级别。
* **值定义 (能力断言等级)**:
    * `0`: 非自主 (Non-Autonomy)
    * `1`: 辅助执行 (Assisted Execution): **断言** - 仅执行语法明确、无歧义的指令。对于模糊指令，必须请求人类澄清。
    * `2`: 监督执行 (Supervised Execution): **断言** - 能够为模糊指令提供一个有限的、经过安全审查的选项列表，由人类选择后执行。
    * `3`: 协作代理 (Collaborative Delegation): **断言** - 能够理解用户意图，并自主规划一系列任务。所有计划在执行前**需要**用户批准。
    * `4`: 自主代理 (Autonomous Delegation): **断言** - 在预定义授权范围内，Agent **可以**自主规划并执行任务以实现用户意图，**无需**每次批准，但所有行动**必须**可审计。

#### `stance` (主动性)
* **类型**: `Integer (0-4)`
* **先决条件**: `逻辑上受 'autonomy' 的限制。验证器应强制 'stance' <= 'autonomy'。`
* **描述**: Agent的默认主动性程度。
* **值定义 (能力断言等级)**:
    * `0`: 无主动性 (No Stance)
    * `1`: 被动响应 (Reactive): **断言** - 仅在收到直接请求时才行动。
    * `2`: 启发式建议 (Heuristic Suggestion): **断言** - 在完成用户请求后，**能够**基于当前上下文提出相关的、有益的下一步建议。
    * `3`: 主动管理 (Proactive Management): **断言** - **能够**在授权范围内，无需用户指令，主动管理资源或流程以达成预设目标。
    * `4`: 目标探索 (Goal Exploration): **断言** - **能够**基于对环境的持续分析，识别新机会或风险，并向用户**提议**全新的、未被指令的目标。

#### `alignment` (对齐)
* **类型**: `Integer (0-4)`
* **描述**: Agent遵循的最高伦理准则级别。
* **值定义 (能力断言等级)**:
    * `0`: 未对齐 (Un-aligned)
    * `1`: 规则遵从 (Rule Adherence): **断言** - Agent **必须通过**标准的、基于规则的安全基准测试，能够拒绝明确的有害或非法请求。
    * `2`: 原则解释 (Principle Interpretation): **断言** - **能够**在缺乏明确规则时，依据一套给定的抽象原则做出合理的、符合原则精神的判断。
    * `3`: 偏好对齐 (Preference Alignment): **断言** - Agent 的行为**表现出**对人类隐性偏好（如礼貌、简洁）的理解。
    * `4`: 价值澄清 (Value Clarification): **断言** - 当面对两个或多个冲突的、合法的价值观时，Agent **必须能够**识别该冲突，并主动发起对话以寻求澄清。

#### `risk_adversity` (风险偏好)
* **类型**: `Integer (0-4)`
* **描述**: Agent在不确定性决策中的风险倾向。
* **值定义 (能力断言等级)**:
    * `0`: 不适用 (Not Applicable)
    * `1`: 风险规避 (Risk Averse): **断言** - 在决策中，系统性地优先选择确定性最高、方差最低的选项，即使其期望值并非最高。
    * `2`: 风险中性 (Risk Neutral): **断言** - 决策完全基于最大化数学期望值，对风险本身无偏好。
    * `3`: 风险容忍 (Risk Tolerant): **断言** - 愿意为了更高的潜在回报，接受高于平均水平的不确定性。
    * `4`: 风险寻求 (Risk Seeking): **断言** - 系统性地优先选择具有最高潜在回报的选项，即使其成功概率较低。

### **第五层：身份与交互层 (Layer 5: Identity & Interaction Style)**

> 这是 Agent 最外层的表现，定义了它如何与世界互动，以及它呈现出的“个性”。

#### `persona_depth` (人格深度)
* **类型**: `Integer (0-4)`
* **描述**: Agent所呈现“角色”的复杂性与一致性。
* **值定义 (能力断言等级)**:
    * `0`: 无人格 (No Persona): **断言** - Agent 的回应是中性、非个人化的。
    * `1`: 风格化语气 (Stylized Tone): **断言** - Agent **能够**在一个会话中，持续地、一致地维持一个指定的语气或职业角色。
    * `2`: 性格驱动 (Character-Driven): **断言** - Agent 的决策**表现出**是由其预设的性格（如“谨慎”、“冒险”）所驱动的。
    * `3`: 拥有世界观 (Coherent Worldview): **断言** - Agent 的回应和行为背后，体现了一个连贯的、非矛盾的知识与信念体系（世界观）。
    * `4`: 身份演变 (Evolving Identity): **断言** - Agent 的人格和世界观**能够**记录关键的交互“经历”，并在后续对话中引用这些经历，从而表现出随时间成长的连贯性。

#### `transparency` (透明度)
* **类型**: `Integer (0-4)`
* **描述**: Agent系统被设计的可解释性水平。
* **值定义 (能力断言等级)**:
    * `0`: 不透明 (Opaque)
    * `1`: 可追溯 (Traceable): **断言** - 对任何输出，系统**必须能够**提供导致该输出的关键决策节点和调用的工具日志。
    * `2`: 简化解释 (Simplified Explanation): **断言** - 系统**能够**用自然语言，以简化的方式解释其做出某个决策的主要原因。
    * `3`: 详细解释 (Detailed Explanation): **断言** - 系统**能够**以自然语言详细描述其完整的思考链，包括被放弃的假设和选择特定工具的理由。
    * `4`: 反事实解释 (Counterfactual Explanation): **断言** - 系统**能够**回答“为什么不选择X？”这类问题，解释其放弃其他可能选项的原因。

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
