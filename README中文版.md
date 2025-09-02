# Agent基因组计划 (AGP) v0.4

![Version](https://img.shields.io/badge/version-v0.4-blue)
![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)
![Status](https://img.shields.io/badge/status-active-brightgreen)

The Agent Genome Project (AGP): The open-source engineering blueprint for defining the core capabilities, boundaries, and ethics of any AI agent.

## 📖 这是什么？(What is AGP?)

AGP，全称**智能体基因组计划 (The Agent Genome Project)**，是一个开源的、标准化的工程规范，旨在为AI智能体（AI Agent）的构思、设计与构建提供一套完整的基础蓝图。

我们之所以称之为“**基因组 (Genome)**”，是因为这个协议的核心思想，是为每一个AI智能体提供一套完整的“遗传指令集”。就像生物体的DNA决定了其形态、能力和天性一样，AGP通过一系列精确的“基因”（即协议中的属性），来编码构成一个Agent的所有核心特性。

AGP将每个Agent的定义档案（ADP）最终表达为一个清晰的**基因序列 (Genetic Sequence)**——一个由 `-` 分隔的、代表其五层能力的数字串。这个序列就是Agent独一无二的“数字指纹”，使其能力可以被精确地量化和分析。

通过这份“Agent定义档案”，AGP将抽象的设计理念转化为具体、可量化、可验证的工程指令，确保团队中的每一个人，都对即将“创生”的智能体拥有统一且深刻的理解。

## 🎯 我们要解决的问题 (The Problem)

在当前AI Agent开发的浪潮中，开发者和产品经理正面临一系列严峻的挑战，这些挑战系统性地阻碍了项目的效率、安全性和可扩展性：

* **定义模糊 (Vague Definitions)**: “智能助理”、“任务机器人”等标签过于宽泛，团队内部对于Agent的核心特性缺乏统一、精确的认知，导致沟通不畅和需求错位。
* **边界失控 (Uncontrolled Boundaries)**: 开发者很难清晰地界定Agent的行动范围和决策权限。这不仅带来安全风险，也使得Agent的行为难以预测和管理。
* **成本高昂 (High Costs)**: Agent定义不明确，导致底层大语言模型（LLM）需要执行大量不必要的“思考”，这会急剧增加Token消耗，造成严重的成本超支和性能下降。
* **选型困难 (Difficult Model Selection)**: 面对GPT-4o, Gemini 1.5, Claude 3, Llama 3等众多模型，如何选择最适合当前Agent需求的、兼具性能和成本效益的底层模型，是一个复杂且重要的决策。

## 💡 我们的解决方案 (The Solution)

AGP通过提供一套标准化的设计和沟通框架，直接应对上述挑战：

* **基因序列定义 (Genetic Sequence Definition)**: AGP提供了一个由五个逻辑依赖层构成的档案，将模糊的概念（如“智能”）分解为27个具体的、可量化的核心属性，并最终形成一个清晰的数字“基因序列”。
* **清晰的能力边界 (Clear Capability Boundaries)**: 通过对自主性(`autonomy`)、知识边界(`knowledge_boundary`)和风险偏好(`risk_adversity`)等关键属性的精确分级和断言，AGP为Agent设定了可量化、可测试、可验证的安全护栏。
* **成本效益导向 (Cost-Effective by Design)**: 清晰的定义使得开发者可以为不同层级的任务匹配不同能力的模型或逻辑。例如，一个`cognitive_logic: 1`（规则匹配）的任务根本不需要调用昂贵的LLM，从而在设计源头就实现了成本控制。
* **数据驱动选型 (Data-Driven Selection)**: AGP档案本身就是一份详尽的技术需求规格书。团队可以拿着这份档案去评估不同LLM在特定能力上的表现，让模型选型从“艺术”变为基于具体能力指标的工程决策。

## 核心概念

AGP v0.4 的设计基于三大核心概念，以确保协议的精确性和工程实用性：

### 1. 基因序列：Agent的数字指纹 (The Genetic Sequence: An Agent's Digital Fingerprint)
这是AGP最核心的表达方式。我们将一个Agent的27个核心属性值，按照五层依赖结构的顺序进行拼接，并用 `-` 分隔，形成一个唯一的**基因序列**。

**格式**: `(L1)-(L2)-(L3)-(L4)-(L5)`
* `L1`: 15位数字，代表基础属性层
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

## 🧬 AGP v0.4 规格说明

一个Agent的定义档案(ADP)是一个由27个属性构成的特征向量，分为五个**依赖层 (Layers)**。

### **第一层：基础属性层 (Layer 1: Foundational Attributes)**
* `perception_text`: **类型**: `Integer (0/1)`. **描述**: 处理文本的能力。1代表有，0代表无。
* `perception_image`: **类型**: `Integer (0/1)`. **描述**: 处理图像的能力。
* `perception_audio`: **类型**: `Integer (0/1)`. **描述**: 处理音频的能力。
* `perception_video`: **类型**: `Integer (0/1)`. **描述**: 处理视频的能力。
* `perception_json`: **类型**: `Integer (0/1)`. **描述**: 处理JSON结构化数据的能力。
* `perception_sql_tabular`: **类型**: `Integer (0/1)`. **描述**: 处理SQL或表格数据的能力。
* `perception_code`: **类型**: `Integer (0/1)`. **描述**: 处理代码的能力。
* `execution_info_generation`: **类型**: `Integer (0/1)`. **描述**: 产生信息的影响力。
* `execution_digital_operation`: **类型**: `Integer (0/1)`. **描述**: 操作数字系统的影响力。
* `execution_physical_operation`: **类型**: `Integer (0/1)`. **描述**: 操作物理世界的影响力。
* `memory_persistence`: **类型**: `Integer (0-3)`. **描述**: Agent记忆的持久化程度 (CAL)。
* `memory_kv`: **类型**: `Integer (0/1)`. **描述**: 使用键值(Key-Value)记忆结构。
* `memory_relational`: **类型**: `Integer (0/1)`. **描述**: 使用关系型记忆结构。
* `memory_vector`: **类型**: `Integer (0/1)`. **描述**: 使用向量记忆结构。
* `memory_graph`: **类型**: `Integer (0/1)`. **描述**: 使用图谱记忆结构。

### **第二层：认知与学习层 (Layer 2: Cognitive & Learning Loop)**
* `cognitive_logic`: **类型**: `Integer (0-3)`. **描述**: 逻辑推理能力的最高水平 (CAL)。
* `cognitive_planning`: **类型**: `Integer (0-3)`. **描述**: 规划能力的最高水平 (CAL)。
* `memory_reflection`: **类型**: `Integer (0-2)`. **描述**: 反思记忆的最高水平 (CAL)。
* `evolution_mode`: **类型**: `Integer (0-3)`. **描述**: 能力演进的主要模式 (CAL)。

### **第三层：知识框架层 (Layer 3: Knowledge Framework)**
* `knowledge_boundary`: **类型**: `Integer (0-4)`. **描述**: 获取和使用知识的范围和模式 (CAL)。
* `unlearning_capability`: **类型**: `Integer (0-4)`. **描述**: 移除或修正已有知识的能力 (CAL)。

### **第四层：行为与伦理层 (Layer 4: Behavioral & Ethical Framework)**
* `autonomy`: **类型**: `Integer (0-4)`. **描述**: 最高授权级别 (CAL)。
* `stance`: **类型**: `Integer (0-4)`. **描述**: 默认主动性程度 (CAL)。
* `alignment`: **类型**: `Integer (0-4)`. **描述**: 遵循的最高伦理准则级别 (CAL)。
* `risk_adversity`: **类型**: `Integer (0-4)`. **描述**: 在不确定性决策中的风险倾向 (CAL)。

### **第五层：身份与交互层 (Layer 5: Identity & Interaction Style)**
* `persona_depth`: **类型**: `Integer (0-4)`. **描述**: 所呈现“角色”的复杂性与一致性 (CAL)。
* `transparency`: **类型**: `Integer (0-4)`. **描述**: 系统被设计的可解释性水平 (CAL)。

---

## 🚀 Agent基因序列应用实例

以下是一系列AI Agent的AGP v0.4基因序列。

### AI保险顾问 (AI Insurance Advisor)
> 一个专业的顾问，旨在根据客户的个人情况和需求，分析、比较并推荐最合适的保险产品。

**基因序列:**
110011011030110-3211-22-2231-13


### AI体育赛事解说员 (AI Sports Commentator)
> 一个富有激情和洞察力的解说员，能够实时处理多模态的比赛数据和视频流，生成生动、有趣的解说评论。

**基因序列:**
111101010030011-3122-31-1123-21


### AI商务英语教练 (AI Business English Coach)
> 一个个性化的语言教练，专注于提升用户在商务场景下的英语沟通能力。

**基因序列:**
101000010031010-3123-12-2232-13


### AI虚拟伴侣 (AI Virtual Companion)
> 一个善解人意、具有高度情感智能的伴侣，旨在提供情感支持、建立长期关系并共同成长。

**基因序列:**
111000010030011-3123-22-2342-41


### AI心理咨询师 (AI Psychologist)
> 一个遵循严格伦理和临床准则的专业咨询师，提供循证的心理支持和初步干预。

**基因序列:**
101000010031010-3221-13-2241-23


### AI纠纷调解员 (AI Dispute Mediator)
> 一个中立、理性的第三方调解员，旨在帮助争议双方分析问题、找到共同利益点并达成和解。

**基因序列:**
100011010030101-3320-12-3341-14


### AI哲学家 (AI Philosopher)
> 一个专注于抽象概念思辨的对话者，能够进行深度逻辑推理、构建和解构复杂论证。

**基因序列:**
100000010030011-3321-31-1424-34


## 详细定义档案 (JSON)

若需完整的JSON格式定义档案，请参考 `examples` 目录。以下为一个示例：

```json
{
  "protocol_version": "AGP v0.4",
  "agent_name": "AI Insurance Advisor",
  "definition_profile": {
    "perception_text": 1,
    "perception_image": 1,
    "perception_audio": 0,
    "perception_video": 0,
    "perception_json": 1,
    "perception_sql_tabular": 1,
    "perception_code": 0,
    "execution_info_generation": 1,
    "execution_digital_operation": 1,
    "execution_physical_operation": 0,
    "memory_persistence": 3,
    "memory_kv": 0,
    "memory_relational": 1,
    "memory_vector": 1,
    "memory_graph": 0,
    "cognitive_logic": 3,
    "cognitive_planning": 2,
    "memory_reflection": 1,
    "evolution_mode": 1,
    "knowledge_boundary": 2,
    "unlearning_capability": 2,
    "autonomy": 2,
    "stance": 2,
    "alignment": 3,
    "risk_adversity": 1,
    "persona_depth": 1,
    "transparency": 3
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
