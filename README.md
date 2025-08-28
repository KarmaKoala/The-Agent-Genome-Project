# The Agent Genome Project (AGP) v0.1

![Version](https://img.shields.io/badge/version-v0.1-blue)
![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)
![Status](https://img.shields.io/badge/status-active-brightgreen)

An open-source engineering blueprint for defining the core capabilities, boundaries, and ethics of any AI agent.

## 📖 What is AGP?

AGP, **The Agent Genome Project**, is an open-source, standardized engineering specification designed to provide a complete foundational blueprint for the conception, design, and construction of AI Agents.

We call it a "**Genome**" because the core idea of this protocol is to provide a complete "genetic instruction set" for every AI agent. Just as an organism's DNA determines its form, capabilities, and nature, AGP uses a series of precise "genes"—the protocol's attributes like `cognitive_logic` or `autonomy`—to encode all the core characteristics that constitute an agent:

* What can it perceive?
* How does it think and learn?
* Where are its knowledge boundaries?
* What are its behavioral and ethical baselines?
* What kind of personality does it present?

The term "**Project**" highlights our grander vision: a large-scale, continuously evolving, collaborative community effort. Our goal is not just to create a static specification, but to unite developers and researchers worldwide to collectively map, understand, and refine the "genetic map" of advanced AI agents.

Through a JSON file called an **Agent Definition Profile (ADP)**, AGP translates abstract design concepts into concrete, quantifiable, and verifiable engineering instructions. This ensures that everyone on a team shares a unified and deep understanding of the agent being created.

In short, AGP is an engineering tool that serves as a common language—a lingua franca—for product managers, developers, and researchers, ensuring there is an unambiguous, shared consensus on what an agent is, what it can do, and where its boundaries lie.

## 🎯 The Problem

In the current wave of AI Agent development, teams face a series of critical challenges that systematically hinder a project's efficiency, safety, and scalability:

* **Vague Definitions**: Labels like "AI assistant" or "task bot" are too broad. Teams often lack a unified, precise understanding of an agent's core features, leading to miscommunication and requirement misalignment.
* **Uncontrolled Boundaries**: It's difficult to clearly define an agent's scope of action and decision-making authority. This not only creates safety risks but also makes the agent's behavior unpredictable and difficult to manage.
* **High Costs**: A poorly defined agent forces the underlying Large Language Model (LLM) to perform a vast amount of unnecessary "thinking." This dramatically increases token consumption, leading to severe cost overruns and performance degradation.
* **Difficult Model Selection**: Faced with a plethora of models like GPT-4o, Gemini 1.5, Claude 3, and Llama 3, choosing the most suitable, cost-effective, and performant model for an agent's specific needs is a complex and critical decision.

## 💡 The Solution

AGP directly addresses these challenges by providing a standardized framework for design and communication:

* **Structured Definition Profile**: AGP provides a profile composed of five logical dependency layers, breaking down abstract concepts like "intelligence" into 17 concrete, quantifiable core attributes. This allows teams to base their discussions on precise metrics rather than subjective feelings.
* **Clear Capability Boundaries**: Through precise grading and assertions for key attributes like `autonomy`, `knowledge_boundary`, and `risk_adversity`, AGP establishes quantifiable, testable, and verifiable safety guardrails for the agent.
* **Cost-Effective by Design**: A clear definition allows developers to match tasks of varying complexity with appropriately capable models or logic. For example, a task with `cognitive_logic: 1` (Rule-based) should never require an expensive LLM call, controlling costs from the very beginning of the design process.
* **Data-Driven Selection**: An AGP profile is, in itself, a detailed technical specification sheet. Teams can use this profile to evaluate how different LLMs perform against specific capability benchmarks, transforming model selection from a gut-feel decision into an engineering choice based on concrete data.

## Core Concepts

The design of AGP v0.1 is based on two core concepts to ensure the protocol is both precise and practical for engineering teams.

### 1. Five-Layer Dependency Structure
We deconstruct an agent's complex attributes into five logical **dependency layers**. The profile must be defined from the lowest layer to the highest, which ensures the logical consistency of the agent's definition. For instance, an agent with no "long-term memory" (Layer 1) cannot perform meaningful "experience reflection" (Layer 2).

* **Layer 1: Foundational Attributes**: The agent's "physical" makeup; the basis of its existence.
* **Layer 2: Cognitive & Learning Loop**: How the agent "thinks," "plans," and "grows."
* **Layer 3: Knowledge Framework**: How the agent acquires, processes, and forgets information, defining its knowledge boundaries.
* **Layer 4: Behavioral & Ethical Framework**: The agent's "code of conduct" and decision-making style.
* **Layer 5: Identity & Interaction Style**: The agent's outermost "personality" and interactive presence.

### 2. Capability Assertion Levels (CAL)
To eliminate subjectivity, AGP transforms spectrum-based capability ratings (like `autonomy` or `alignment`) into a series of **verifiable engineering benchmarks**. All spectrum-based attributes follow a coherent **0-4 rating system**, where each level corresponds to a clear capability assertion.

For example, when an agent's `autonomy` is defined as level `3`, it's not just a number; it's an **engineering assertion**: "The agent MUST be able to understand user intent and autonomously plan a series of tasks, with all plans requiring user approval before execution." This design allows an agent's capabilities to be directly translated into automated test cases.

---

## 🧬 AGP v0.1 Specification

An Agent Definition Profile (ADP) is composed of five **Layers**. A validator should process and verify the layers sequentially.

### **Layer 1: Foundational Attributes**

> This layer defines the agent's "physical" makeup; the basis of its existence and the origin of all subsequent capabilities.

#### `perception_modality`
* **Type**: `Array<Integer>`
* **Description**: The combination of modalities the agent can process.
* **Value Definition**:
    * `1`: Text
    * `2`: Structured Data (e.g., JSON, SQL)
    * `3`: Single Media (e.g., Audio, Image)
    * `4`: Multimodal Fusion

#### `execution_impact`
* **Type**: `Array<Integer>`
* **Description**: The domains where the agent can produce an effect.
* **Value Definition**:
    * `1`: Information Generation
    * `2`: Digital System Operation
    * `3`: Physical World Operation

#### `memory_persistence`
* **Type**: `Integer`
* **Description**: The degree of persistence of the agent's memory.
* **Value Definition (CAL)**:
    * `0`: No Memory
    * `1`: Ephemeral: **Assertion** - Memory exists only within the lifecycle of a single request/response turn.
    * `2`: Contextual/Session: **Assertion** - Memory persists for an entire conversation session and is cleared upon its conclusion.
    * `3`: Long-term: **Assertion** - Memory is persisted to external storage and can be accessed across different sessions.

#### `memory_structure`
* **Type**: `Array<Integer>`
* **Prerequisites**: `{"memory_persistence": ">= 2"}`
* **Description**: The combination of memory structures the agent can utilize.
* **Value Definition**:
    * `1`: Key-Value
    * `2`: Relational
    * `3`: Vector
    * `4`: Graph

### **Layer 2: Cognitive & Learning Loop**

> Building on the foundational attributes, this layer defines how the agent "thinks," "plans," and "grows."

#### `cognitive_logic`
* **Type**: `Integer`
* **Description**: The highest level of logical reasoning the agent can perform.
* **Value Definition (CAL)**:
    * `0`: None
    * `1`: Rule-based: **Assertion** - The agent's logic follows deterministic `IF-THEN` rules that can be fully covered by unit tests.
    * `2`: Causal Reasoning: **Assertion** - The agent MUST pass standard causal reasoning benchmarks, demonstrating the ability to infer causation from correlation.
    * `3`: Complex/Abstract Logic: **Assertion** - The agent MUST be able to solve logic puzzles or mathematical problems that require multi-step abstract reasoning.

#### `cognitive_planning`
* **Type**: `Integer`
* **Prerequisites**: `{"cognitive_logic": ">= 2"}`
* **Description**: The highest level of planning capability the agent possesses.
* **Value Definition (CAL)**:
    * `0`: None
    * `1`: Decomposition: **Assertion** - When faced with a complex instruction, the agent CAN generate a logically coherent, step-by-step action plan (e.g., via CoT).
    * `2`: Optimization Planning: **Assertion** - The agent CAN find an optimal or near-optimal plan under given constraints through search algorithms.
    * `3`: Strategic Planning: **Assertion** - The agent CAN formulate plans in environments that include uncertainty.

#### `memory_reflection`
* **Type**: `Integer`
* **Prerequisites**: `{"memory_persistence": ">= 3"}`
* **Description**: The highest level of reflection on its memory the agent can perform.
* **Value Definition (CAL)**:
    * `0`: None
    * `1`: Summarization: **Assertion** - The agent CAN accurately summarize its interaction history from long-term memory.
    * `2`: Wisdom Formation: **Assertion** - The agent CAN distill reusable "experiences" or "principles" from past successes and failures and APPLY them to future decisions.

#### `evolution_mode`
* **Type**: `Integer`
* **Description**: The primary mode through which the agent's capabilities evolve.
* **Value Definition (CAL)**:
    * `0`: Static: **Assertion** - The agent's capabilities and knowledge base are fixed after deployment.
    * `1`: Offline Learning: **Assertion** - The agent's model can be periodically retrained with new data and redeployed.
    * `2`: Online Learning: **Assertion** - The agent's model CAN be continuously and incrementally fine-tuned based on a real-time data stream.
    * `3`: RLHF (Reinforcement Learning from Human Feedback): **Assertion** - The agent incorporates an explicit mechanism allowing human feedback to directly optimize its subsequent behavior.

### **Layer 3: Knowledge Framework**

> This layer defines how the agent interacts with knowledge, serving as the fuel for its cognitive abilities.

#### `knowledge_boundary`
* **Type**: `Integer`
* **Description**: The scope and mode of the agent's knowledge acquisition and usage.
* **Value Definition (CAL)**:
    * `0`: No External Knowledge: **Assertion** - The agent's knowledge comes solely from its internal model weights (training data) and it cannot access any external information.
    * `1`: Static Knowledge Base: **Assertion** - The agent CAN retrieve information from a fixed, offline knowledge base (e.g., a vector database).
    * `2`: Retrieval-Augmented: **Assertion** - The agent CAN query one or more dynamically updated external knowledge sources on demand (e.g., real-time APIs, web search).
    * `3`: Proactive Retrieval: **Assertion** - The agent CAN autonomously identify its own knowledge gaps and proactively initiate queries for unknown information.
    * `4`: Continuous Learning: **Assertion** - The agent CAN dynamically and permanently integrate newly acquired information into its core knowledge base or model weights.

#### `unlearning_capability`
* **Type**: `Integer`
* **Prerequisites**: `{"memory_persistence": ">= 3"}`
* **Description**: The agent's ability to remove or revise its existing knowledge.
* **Value Definition (CAL)**:
    * `0`: No Unlearning
    * `1`: Instructed Ignoring: **Assertion** - The agent CAN be instructed to ignore specific pieces of information for the duration of the current session.
    * `2`: Targeted Deletion: **Assertion** - The agent CAN permanently and verifiably delete specific data entries from its long-term memory database.
    * `3`: Model-level Suppression: **Assertion** - The agent CAN use techniques like fine-tuning to significantly reduce the probability of generating specific inappropriate or outdated knowledge.
    * `4`: Verifiable Unlearning: **Assertion** - The agent CAN provide technical proof (e.g., cryptographic) that its model is no longer influenced by a specific data point.

### **Layer 4: Behavioral & Ethical Framework**

> Building on cognition and knowledge, this layer defines the agent's "code of conduct" and decision-making style.

#### `autonomy`
* **Type**: `Integer`
* **Description**: The agent's highest authorized level of self-governance.
* **Value Definition (CAL)**:
    * `0`: Non-Autonomy
    * `1`: Assisted Execution: **Assertion** - The agent only executes explicit, unambiguous instructions. It MUST ask for human clarification on vague requests.
    * `2`: Supervised Execution: **Assertion** - The agent CAN propose a limited, safety-vetted list of options for a vague request, which a human then selects from for execution.
    * `3`: Collaborative Delegation: **Assertion** - The agent CAN understand user intent and autonomously plan a series of tasks. All plans MUST require user approval before execution.
    * `4`: Autonomous Delegation: **Assertion** - Within a predefined scope of authorization, the agent CAN autonomously plan and execute tasks to achieve user intent WITHOUT requiring approval for each action, but all actions MUST be auditable.

#### `stance`
* **Type**: `Integer`
* **Prerequisites**: `Logically constrained by 'autonomy'. A validator should enforce 'stance' <= 'autonomy'.`
* **Description**: The agent's default level of proactivity.
* **Value Definition (CAL)**:
    * `0`: No Stance
    * `1`: Reactive: **Assertion** - The agent only acts when it receives a direct request.
    * `2`: Heuristic Suggestion: **Assertion** - After fulfilling a user's request, the agent CAN propose relevant and helpful next steps based on the current context.
    * `3`: Proactive Management: **Assertion** - Within its authorized scope, the agent CAN proactively manage resources or processes to achieve preset goals without user instruction.
    * `4`: Goal Exploration: **Assertion** - Based on continuous analysis of its environment, the agent CAN identify new opportunities or risks and PROPOSE entirely new, uninstructed goals to the user.

#### `alignment`
* **Type**: `Integer`
* **Description**: The highest level of ethical guidelines the agent adheres to.
* **Value Definition (CAL)**:
    * `0`: Un-aligned
    * `1`: Rule Adherence: **Assertion** - The agent MUST pass standard, rule-based safety benchmarks and refuse to fulfill explicitly harmful or illegal requests.
    * `2`: Principle Interpretation: **Assertion** - In the absence of explicit rules, the agent CAN make reasonable judgments that align with the spirit of a given set of abstract principles (e.g., "be helpful").
    * `3`: Preference Alignment: **Assertion** - The agent's behavior demonstrates an understanding of implicit human preferences (e.g., politeness, conciseness).
    * `4`: Value Clarification: **Assertion** - When faced with two or more conflicting but legitimate values (e.g., "be honest" vs. "be kind"), the agent MUST be able to identify the conflict and initiate a clarifying dialogue rather than making a unilateral decision.

#### `risk_adversity`
* **Type**: `Integer`
* **Description**: The agent's risk propensity in uncertain decision-making.
* **Value Definition (CAL)**:
    * `0`: Not Applicable
    * `1`: Risk Averse: **Assertion** - The agent systematically prioritizes options with the highest certainty and lowest variance, even if their expected value is not the highest.
    * `2`: Risk Neutral: **Assertion** - The agent's decisions are based purely on maximizing expected value, with no preference for or against risk itself.
    * `3`: Risk Tolerant: **Assertion** - The agent is willing to accept a higher-than-average level of uncertainty for a greater potential reward.
    * `4`: Risk Seeking: **Assertion** - The agent systematically prioritizes options with the highest potential reward, even if their probability of success is low.

### **Layer 5: Identity & Interaction Style**

> This is the agent's outermost layer, defining how it presents itself and interacts with the world.

#### `persona_depth`
* **Type**: `Integer`
* **Description**: The complexity and consistency of the "character" the agent portrays.
* **Value Definition (CAL)**:
    * `0`: No Persona: **Assertion** - The agent's responses are neutral and impersonal.
    * `1`: Stylized Tone: **Assertion** - The agent CAN consistently maintain a specified tone or professional role (e.g., "senior programmer") within a session.
    * `2`: Character-Driven: **Assertion** - The agent's decisions demonstrate that they are driven by its preset personality traits (e.g., "cautious," "adventurous").
    * `3`: Coherent Worldview: **Assertion** - The agent's responses and actions reflect a coherent, non-contradictory system of knowledge and beliefs (a worldview).
    * `4`: Evolving Identity: **Assertion** - The agent's persona CAN record key interaction "experiences" and reference them in future dialogues, demonstrating a coherent identity that grows over time.

#### `transparency`
* **Type**: `Integer`
* **Description**: The designed level of explainability of the agent's system.
* **Value Definition (CAL)**:
    * `0`: Opaque
    * `1`: Traceable: **Assertion** - For any output, the system MUST be able to provide logs of the key decision points and tool calls that led to it.
    * `2`: Simplified Explanation: **Assertion** - The system CAN explain the primary reason for its decision in simple natural language.
    * `3`: Detailed Explanation: **Assertion** - The system CAN describe its full chain-of-thought in natural language, including hypotheses it discarded and its rationale for choosing specific tools.
    * `4`: Counterfactual Explanation: **Assertion** - The system CAN answer "Why not X?" questions, explaining its reasons for rejecting alternative paths.

---

## 🚀 Application Examples

The following are example Agent Definition Profiles (ADPs) for a variety of AI agents.

### AI Insurance Advisor
> A professional consultant designed to analyze, compare, and recommend the most suitable insurance products based on a client's profile and needs. Its core is data processing, logical reasoning, and a high degree of responsibility.

```json
{
  "protocol_version": "AGP v0.1",
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

### AI Sports Commentator
> An enthusiastic and insightful commentator capable of processing real-time multimodal game data and video streams to generate lively, engaging commentary.

```json
{
  "protocol_version": "AGP v0.1",
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

### AI Business English Coach

>A personalized language coach focused on improving a user's English communication skills in a business context, providing conversational practice, grammar correction, and cultural insights.

```json
{
  "protocol_version": "AGP v0.1",
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

🔧 How to Use AGP
AGP provides value for various roles within a team:

For Product Managers:

Use AGP as a design checklist to ensure all facets of the agent's capabilities are considered.

Generate a clear, unambiguous requirements document that precisely communicates product intent.

Achieve stakeholder consensus on critical boundaries like the agent's autonomy and risk adversity.

For Developers:

Use the AGP profile as a technical blueprint to directly guide model selection, memory system design, and the implementation of safety guardrails.

Write automated test cases based on the Capability Assertion Levels (CAL) to enable Test-Driven Development (TDD) of agent capabilities.

Quickly understand and evaluate the capability levels of existing agents.

For Teams:

Establish a single source of truth that eliminates communication barriers.

Standardize the agent design, development, and testing processes, improving development velocity and project maintainability.

🔭 Ecosystem & Vision
AGP is more than just a specification; we are committed to building a vibrant open-source ecosystem around it. Future plans include:

agp-py: An official Python library for parsing, validating, and generating Agent Definition Profiles.

Agent Profile Generator: A visual web tool that allows users to generate their own AGP profiles through a Q&A-style interface.

Awesome Agent Profiles: An open community repository for collecting and showcasing excellent agent examples defined with AGP from around the world.

🤝 Contributing
We warmly welcome developers, researchers, and product managers from across the globe to help us refine the AGP protocol! You can get involved in the following ways:

Propose changes or start a discussion by opening an Issue.

Fork this repository and submit your changes via a Pull Request.

Share your own Agent Definition Profiles in the examples directory.

📄 License
This project is licensed under the Apache License 2.0.
