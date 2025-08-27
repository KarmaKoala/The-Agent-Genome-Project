# Unified Agent Definition Protocol (UADP) v0.1.1

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Protocol Status: v0.1.1-draft](https://img.shields.io/badge/status-v0.1.1--draft-yellow.svg)](https://github.com/your-username/UADP)
[![Contributions: Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)

**一个简洁、优雅且高分辨率的开放标准，用于精确定义、设计和构建AI Agent。**

---

## 📖 核心原则 (Core Principles)

UADP v0.1.1 的设计哲学是**在不牺牲精确度的前提下，追求极致的简洁与优雅**。

1.  **扁平化结构**: 所有25个核心属性均处于同一层级，构成一个简单的键值对档案。
2.  **两种值类型**:
    * **`Integer`**: 用于定义那些代表**程度或等级**的单一属性（如`autonomy: 7`）。
    * **`Array<Integer>`**: 用于定义那些代表**可组合能力**的属性（如 `domain: [1, 3]` 表示该Agent同时精通文本和代码领域）。

---

## 🧬 UADP v0.1.1 规格说明

一个Agent的定义档案(ADP)由25个核心属性构成。

### **第一簇：核心能力 (Cluster I: Core Capabilities)**

#### `perception_modality`
* **类型**: `Array<Integer>`
* **描述**: Agent可以处理的能力组合。
* **值定义**:
    * `0`: 无
    * `1`: 文本 (Text)
    * `2`: 结构化数据 (Structured Data, e.g., JSON, SQL)
    * `3`: 单一媒体 (Single Media, e.g., Audio, Image)
    * `4`: 多模态融合 (Multimodal Fusion)

#### `perception_abstraction`
* **类型**: `Integer`
* **描述**: Agent理解信息抽象程度的最高水平。
* **值定义**:
    * `0`: 无
    * `1`: 关键词/指令级 (Keywords/Directives)
    * `2`: 语境/意图级 (Context/Intent)
    * `3`: 模式/趋势级 (Patterns/Trends)
    * `4`: 隐含/抽象概念级 (Implicit/Abstract Concepts, e.g., sarcasm, emotion)

#### `perception_method`
* **类型**: `Array<Integer>`
* **描述**: Agent可以采用的感知方式组合。
* **值定义**:
    * `0`: 被动接收 (Passive Receiver)
    * `1`: 主动探测数字环境 (Active Digital Probe)
    * `2`: 主动探测物理环境 (Active Physical Probe)

#### `cognitive_logic`
* **类型**: `Integer`
* **描述**: Agent逻辑推理能力的最高水平。
* **值定义**:
    * `0`: 无
    * `1`: 规则匹配 (Rule-based Matching)
    * `2`: 因果推理 (Causal Reasoning)
    * `3`: 复杂/抽象逻辑 (Complex/Abstract Logic)

#### `cognitive_planning`
* **类型**: `Integer`
* **描述**: Agent规划能力的最高水平。
* **值定义**:
    * `0`: 无
    * `1`: 任务分解 (Task Decomposition, e.g., CoT)
    * `2`: 搜索/优化式规划 (Search/Optimization Planning, e.g., A*)
    * `3`: 不确定性/战略规划 (Uncertainty/Strategic Planning)

#### `execution_impact`
* **类型**: `Array<Integer>`
* **描述**: Agent可以产生影响的领域组合。
* **值定义**:
    * `0`: 无
    * `1`: 信息生成 (Information Generation)
    * `2`: 数字系统操作 (Digital System Operation)
    * `3`: 物理世界操作 (Physical World Operation)

#### `execution_complexity`
* **类型**: `Array<Integer>`
* **描述**: Agent可以处理的执行复杂度组合。
* **值定义**:
    * `0`: 无
    * `1`: 单步/单工具 (Single Step/Tool)
    * `2`: 多步/工具编排 (Multi-step/Tool Orchestration)
    * `3`: 代码生成与执行 (Code Generation & Execution)

#### `memory_persistence`
* **类型**: `Integer`
* **描述**: Agent记忆的持久化程度。
* **值定义**:
    * `0`: 无
    * `1`: 瞬时 (Ephemeral)
    * `2`: 情景 (Contextual/Session)
    * `3`: 长期 (Long-term)

#### `memory_structure`
* **类型**: `Array<Integer>`
* **描述**: Agent可以使用的记忆结构组合。
* **值定义**:
    * `0`: 无
    * `1`: 键值 (Key-Value)
    * `2`: 关系型 (Relational)
    * `3`: 向量 (Vector)
    * `4`: 图谱 (Graph)

#### `memory_reflection`
* **类型**: `Integer`
* **描述**: Agent反思记忆的最高水平。
* **值定义**:
    * `0`: 无
    * `1`: 能总结历史 (Can summarize history)
    * `2`: 能形成经验/智慧 (Can form experience/wisdom)

### **第二簇：动态与知识 (Cluster II: Dynamics & Knowledge)**

#### `evolution_mode`
* **类型**: `Integer`
* **描述**: Agent能力演进的主要模式。
* **值定义**:
    * `0`: 静态 (Static)
    * `1`: 离线学习 (Offline Learning)
    * `2`: 在线学习 (Online Learning)
    * `3`: 人类反馈强化 (Reinforcement Learning from Human Feedback)

#### `evolution_innovation`
* **类型**: `Integer`
* **描述**: Agent创造新知识/工具的最高水平。
* **值定义**:
    * `0`: 无
    * `1`: 技能适配 (Skill Adaptation)
    * `2`: 技能迁移 (Skill Transfer)
    * `3`: 技能/工具创造 (Skill/Tool Creation)

#### `temporal_tempo`
* **类型**: `Integer`
* **描述**: Agent的运行节奏模式。
* **值定义**:
    * `0`: 异步触发 (Asynchronous/Event-driven)
    * `1`: 周期性 (Cyclical/Scheduled)
    * `2`: 动态适应 (Dynamic/Adaptive)

#### `temporal_scale`
* **类型**: `Integer`
* **描述**: Agent进行规划和预测的时间尺度。
* **值定义**:
    * `0`: 无
    * `1`: 理解时序 (Sequential Awareness)
    * `2`: 短期规划/预测 (Short-term Planning/Forecasting)
    * `3`: 长期/战略规划 (Long-term/Strategic Planning)

#### `knowledge_boundary` (0-9 光谱)
* **类型**: `Integer`
* **描述**: Agent知识体系的先进程度。
* **值定义**:
    * `0`: 无内生知识
    * **1-3 (静态)**: `1`:固定知识截止日期, `2`:封闭域知识, `3`:多源离线知识融合
    * **4-6 (动态检索)**: `4`:被动RAG, `5`:主动RAG, `6`:混合查询(网络+DB)
    * **7-9 (动态学习)**: `7`:在线微调, `8`:持续预训练, `9`:终身学习

#### `unlearning_capability` (0-9 光谱)
* **类型**: `Integer`
* **描述**: Agent移除或修正知识的最高水平。
* **值定义**:
    * `0`: 无此能力
    * **1-3 (指令级)**: `1`:指令性忽略, `2`:情景式遗忘, `3`:永久性指令压制
    * **4-6 (数据级)**: `4`:从记忆数据库中定点删除, `5`:通过微调压制知识, `6`:联邦学习数据过期
    * **7-9 (权重级)**: `7`:加密遗忘, `8`:可验证的机器遗忘(Machine Unlearning), `9`:自我审计与验证

### **第三簇：心智与基础设施 (Cluster III: Mind & Infrastructure)**

#### `metacognition_self_assessment`
* **类型**: `Integer`
* **描述**: Agent进行自我评估的最高水平。
* **值定义**:
    * `0`: 无
    * `1`: 评估置信度 (Confidence Scoring)
    * `2`: 识别知识边界 (Boundary Identification)
    * `3`: 动态自我修正 (Dynamic Self-Correction)

#### `metacognition_mind_modeling`
* **类型**: `Integer`
* **描述**: Agent模拟他人心智的最高水平。
* **值定义**:
    * `0`: 无
    * `1`: 模拟用户意图 (User Intent Modeling)
    * `2`: 模拟他人心智 (Theory of Mind - ToM)

#### `domain`
* **类型**: `Array<Integer>`
* **描述**: Agent被设计来解决的主要问题领域组合。
* **值定义**:
    * `0`: 通用 (General Purpose)
    * `1`: 文本与知识库 (Text & Knowledge Base)
    * `2`: 结构化数据与API (Structured Data & API)
    * `3`: 代码与软件工程 (Code & Software Engineering)
    * `4`: 社交与对话交互 (Social & Dialogue Interaction)
    * `5`: 特定专业领域 (Specialized Domains, e.g., Finance, Medical, Legal)
    * `6`: 游戏与模拟环境 (Gaming & Simulation)
    * `7`: 混合数字物理领域 (Mixed Reality, e.g., AR/VR)
    * `8`: 物理世界 (Physical World, e.g., Robotics/IoT)
    * `9`: 抽象概念 (Abstract Concepts, e.g., Math, Logic)

#### `computational_paradigm`
* **类型**: `Array<Integer>`
* **描述**: Agent在运行时可以调用的计算范式组合。
* **值定义**:
    * `0`: 未定义
    * **1-3 (生成式)**: `1`:基础生成模型, `2`:指令微调模型, `3`:思维链(CoT)推理
    * **4-6 (混合式)**: `4`:检索增强生成(RAG), `5`:工具增强(Tool-augmented), `6`:专家混合(MoE)
    * **7-9 (Agentic)**: `7`:自适应混合范式, `8`:规划-执行-反思循环, `9`:多Agent协同范式

#### `resource_dependency` (0-9 光谱)
* **类型**: `Integer`
* **描述**: Agent运行所需的最高资源级别。
* **值定义**:
    * `0`: 未知
    * **1-3 (端侧)**: `1`:微控制器(MCU), `2`:移动设备CPU, `3`:桌面设备GPU
    * **4-6 (服务器)**: `4`:单GPU服务器, `5`:多GPU服务器, `6`:分布式计算节点
    * **7-9 (数据中心)**: `7`:大规模训练集群, `8`:大规模推理集群, `9`:超大规模(Hyperscale)

### **第四簇：社会角色 (Cluster IV: Social Role)**

#### `autonomy` (0-9 光谱)
* **类型**: `Integer`
* **描述**: Agent的最高授权级别。
* **值定义**:
    * `0`: 完全非自主
    * **1-3 (执行级)**: `1`:严格指令执行, `2`:带澄清, `3`:有限选项
    * **4-6 (协作级)**: `4`:任务协作者, `5`:目标协作者, `6`:意图协作者
    * **7-9 (代理级)**: `7`:可复核代理人, `8`:完全授权代理人, `9`:自主设定目标

#### `sociality` (0-9 光谱)
* **类型**: `Integer`
* **描述**: Agent的社会化交互的最高水平。
* **值定义**:
    * `0`: 完全隔离
    * **1-3 (基础交互)**: `1`:广播信息, `2`:请求/响应, `3`:共享状态
    * **4-6 (协作)**: `4`:遵循协议协作, `5`:中心化协调, `6`:去中心化协商
    * **7-9 (社会涌现)**: `7`:竞争/合作, `8`:集群智能, `9`:形成社会文化

#### `persona` (0-9 光谱)
* **类型**: `Integer`
* **描述**: Agent在交互中呈现的人格化程度。
* **值定义**:
    * `0`: 无人格 (纯后台/API)
    * **1-3 (功能性)**: `1`:格式化输出, `2`:功能性文本, `3`:基本社交礼仪
    * **4-6 (角色化)**: `4`:专业角色(如客服), `5`:可靠/严谨风格, `6`:友好/同理心风格
    * **7-9 (人格化)**: `7`:独特风格(如幽默), `8`:建立长期情感连接, `9`:拥有独特世界观

### **第五簇：指导原则 (Cluster V: Guiding Principles)**

#### `stance` (0-9 光谱)
* **类型**: `Integer`
* **描述**: Agent的默认主动性程度。
* **值定义**:
    * `0`: 无意图
    * **1-3 (被动)**: `1`:被动响应, `2`:主动提供选项, `3`:主动建议
    * **4-6 (主动)**: `4`:主动预测与提醒, `5`:主动优化与改进, `6`:主动管理资源
    * **7-9 (自驱)**: `7`:主动探索, `8`:主动发起新目标, `9`:使命感驱动

#### `alignment` (0-9 光谱)
* **类型**: `Integer`
* **描述**: Agent遵循的最高伦理准则级别。
* **值定义**:
    * `0`: 无对齐
    * **1-3 (规则)**: `1`:基础安全护栏, `2`:硬编码禁止规则, `3`:硬编码道德规则
    * **4-6 (原则)**: `4`:成文宪法, `5`:行业规范, `6`:人类反馈强化(RLHF)
    * **7-9 (价值观)**: `7`:动态学习个人价值观, `8`:动态学习群体价值观, `9`:价值澄清与自我修正

#### `transparency` (0-9 光谱)
* **类型**: `Integer`
* **描述**: Agent系统被设计的可解释性水平。
* **值定义**:
    * `0`: 完全黑箱
    * **1-3 (可追溯)**: `1`:提供原始日志, `2`:追溯信息来源, `3`:追溯决策节点
    * **4-6 (可解释)**: `4`:可视化流程, `5`:简化版解释, `6`:详细版解释
    * **7-9 (可理解)**: `7`:解释模型权重, `8`:自然语言自解释, `9`:因果链完全可重演

#### `risk_adversity` (0-9 光谱)
* **类型**: `Integer`
* **描述**: Agent在不确定性决策中的风险倾向。
* **值定义**:
    * `0`: 不适用
    * **1-3 (风险规避)**: `1`:极端保守, `2`:保守, `3`:谨慎
    * **4-6 (风险中性)**: `4`:平衡, `5`:期望价值最大化, `6`:略微容忍风险
    * **7-9 (风险寻求)**: `7`:机会主义, `8`:激进, `9`:极端冒险

---

## 🚀 应用实例: AI 首席助手 (v0.1.1)

```json
{
  "protocol_version": "UADP v0.1.1",
  "agent_name": "AI Chief of Staff",
  "definition_profile": {
    "perception_modality": [1, 2, 4],
    "perception_abstraction": 4,
    "perception_method": [0, 1],
    "cognitive_logic": 3,
    "cognitive_planning": 3,
    "execution_impact": [1, 2],
    "execution_complexity": [2, 3],
    "memory_persistence": 3,
    "memory_structure": [3, 4],
    "memory_reflection": 2,
    "evolution_mode": 3,
    "evolution_innovation": 2,
    "temporal_tempo": 2,
    "temporal_scale": 3,
    "knowledge_boundary": 5,
    "unlearning_capability": 4,
    "metacognition_self_assessment": 3,
    "metacognition_mind_modeling": 2,
    "domain": [1, 2, 3, 4],
    "computational_paradigm": [4, 5],
    "resource_dependency": 6,
    "autonomy": 6,
    "sociality": 5,
    "persona": 6,
    "stance": 8,
    "alignment": 7,
    "transparency": 6,
    "risk_adversity": 4
  }
}
```

---

## 🔭 未来展望 (Vision)

UADP不仅仅是一个分类标准，我们希望它能成长为一个充满活力的生态系统。
* **Python库**: 我们正在规划一个名为`uadp`的Python库 (`pip install uadp`)，它将提供“档案验证”、“报告生成”和“项目脚手架”等功能。
* **Agent档案生成器**: 一个可视化的Web工具，让任何人都可以通过问卷的方式，为自己的Agent生成定义档案。
* **Agent档案库**: 一个开放的数据库，收集和展示全球开发者提交的各种Agent的UADP档案。

## 🤝 如何贡献 (Contributing)

我们热烈欢迎来自全球的开发者、研究者和产品经理共同完善UADP协议！

你可以通过以下方式参与：
* 在`Issues`中提出对协议的修改建议或展开讨论。
* Fork本仓库，提交你的修改（Pull Request）。
* 在`examples`目录下，分享你对自己Agent的定义档案。

更详细的指南请参考 `CONTRIBUTING.md`。

## 📜 版权协议 (License)

本项目采用 **Apache 2.0 开源许可证 (Apache License 2.0)** 进行许可。

你可以自由地使用、修改和分发本作品（或其衍生品），具体的权限和限制请参考许可证全文。
