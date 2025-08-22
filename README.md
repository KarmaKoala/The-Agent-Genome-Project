# The E-TIP12 Genome Model

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Project Status: Active](https://img.shields.io/badge/status-active-success.svg)](https://github.com/your-username/E-TIP12)
[![Contributions: Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)

**Mapping the unique Digital DNA for every AI Agent.**

---

## 📖 What is E-TIP12?

**E-TIP12** is an open standard and classification framework designed for the age of AI Agents.

The core idea is to treat every Agent as a unique "digital organism" by defining its **Digital DNA Sequence**—a 12-locus code that precisely describes its capabilities, evolutionary dynamics, interaction patterns, and guiding principles. E-TIP12 provides a universal language to understand, design, and compare increasingly complex AI systems.

## 🎯 The Problem

In the rush of AI Agent development, teams face critical challenges:

* **Vague Definitions:** Labels like "AI Assistant" or "Task Bot" are ambiguous. Teams lack a common, precise vocabulary to define an Agent's core features, leading to miscommunication and requirement gaps.
* **Uncontrolled Boundaries:** Developers struggle to clearly define an Agent's scope of action and decision-making authority. This creates safety risks and makes Agent behavior unpredictable and difficult to manage.
* **High Costs:** A poorly defined Agent leads to inefficient prompting and "thought processes" from the underlying LLM. This dramatically increases token consumption, causing significant cost overruns and performance degradation.
* **Difficult Model Selection:** With a crowded landscape of foundation models (GPT-4o, Gemini 1.5, Claude 3, Llama 3), choosing the most suitable and cost-effective model for a specific Agent's needs is a complex and high-stakes decision.

## 💡 The Solution

**E-TIP12** addresses these challenges head-on:

* **A Universal Language:** The 12-digit E-TIP12 code serves as a unique "fingerprint" for any Agent, providing a precise, unambiguous language for everyone from product managers to engineers.
* **A Constitutional Blueprint:** The E-TIP12 genome acts as an Agent's "constitution." By explicitly defining genes like `Execution (E)`, `Autonomy (A)`, and `Alignment (AL)`, developers can establish clear operational boundaries **before a single line of code is written**.
* **A Cost-Optimization Tool:** A precise E-TIP12 genotype is a powerful tool for cost control. Defining an Agent's `Cognition (C)` gene as `C2 (Causal Reasoning)` instead of `C4 (Metacognitive)`, for instance, guides the creation of leaner system prompts, **preventing the LLM from engaging in expensive, unnecessary recursive thinking, thereby saving tokens**.
* **A Guide for Strategic Decisions:** The E-TIP12 code functions as a "requirements specification" for the foundation model, clarifying and simplifying the selection process.

## 🎯 Strategic Application: Aiding Model Selection

The E-TIP12 genome is a powerful tool for evaluating and selecting the right foundation model. Think of an Agent's "genetic requirements" as its "hardware specifications."

| Required E-TIP12 "Gene" | Recommended Model Type | Examples |
| :--- | :--- | :--- |
| `C4` (Metacognitive), `ST3` (Inquisitive) | **Top-tier Reasoning Models** | GPT-4o, Claude 3 Opus, Gemini 1.5 Pro |
| `P2` (Multi-channel Fusion) | **Powerful Multimodal Models** | GPT-4o, Gemini 1.5 Pro |
| `C1/C2`, `Pe1`, `AL1` | **Cost-effective or Open-Source Models** | Claude 3 Haiku, Llama 3 8B, Mistral Medium |
| `M4` (Reflective Memory), `Tz3` (Strategic) | **Models with Very Long Context Windows** | Gemini 1.5 Pro, Claude 3 series |

---

## 🧬 The E-TIP12 Genetic Coding Standard

### E-Chromosome: Execution Core
**Loci**: 1-3

| Locus | Gene Name | Code | Allele | Core Definition |
| :--- | :--- | :-- | :--- | :--- |
| **1st** | **P - Perception** | 1 | Single-channel | Relies on a single modality of input (e.g., text only). |
| | | 2 | Multi-channel Fusion | Can integrate and understand multiple, diverse input modalities. |
| | | 3 | Active Exploration | Can actively probe its environment (digitally or physically) to gather information. |
| **2nd** | **C - Cognition** | 1 | Pattern Matching | Operates on simple, rule-based or direct-response patterns. |
| | | 2 | Causal Reasoning | Understands "if-then" logic and can make simple inferences. |
| | | 3 | Strategic Planning | Can decompose long-term goals into sequential tasks and plans. |
| | | 4 | Metacognitive | Can assess its own knowledge confidence, identify its boundaries, and handle uncertainty. |
| **3rd** | **E - Execution** | 0 | Self-Regulation | Acts only internally, e.g., by optimizing its own parameters or memory. |
| | | 1 | Digital World | Acts within digital environments, e.g., calling APIs, generating content, operating software. |
| | | 2 | Physical World | Acts on the physical environment through robotic actuators, IoT devices, etc. |

### T-Chromosome: Temporal Dynamics
**Loci**: 4-6

| Locus | Gene Name | Code | Allele | Core Definition |
| :--- | :--- | :-- | :--- | :--- |
| **4th** | **EV - Evolution** | 1 | Fixed | Capabilities and knowledge are static post-deployment. |
| | | 2 | Adaptive | Can adjust its behavioral strategies based on feedback, but its core model is unchanged. |
| | | 3 | Learning | Can update its core model or knowledge base with new data, enabling capability growth. |
| | | 4 | Creative | Can synthesize novel knowledge, skills, or methodologies beyond its training data. |
| **5th** | **M - Memory** | 1 | Ephemeral | Stateless; memory is wiped after each interaction. |
| | | 2 | Contextual | Retains context within a single, continuous session or conversation. |
| | | 3 | Persistent | Has a long-term, read-write memory store that persists across sessions. |
| | | 4 | Reflective | Can reason about and learn from its own past memories to form "experience" or "wisdom." |
| **6th** | **Tz - Temporal Horizon** | 0 | Asynchronous | Dormant; purely event-driven with no internal "heartbeat." |
| | | 1 | Cyclical | Operates on a fixed, predictable schedule (e.g., hourly, daily). |
| | | 2 | Dynamic | Can adapt its operational tempo based on environmental urgency and priorities. |
| | | 3 | Strategic | Paces its actions based on a long-term vision, exhibiting "strategic patience." |

### I-Chromosome: Interaction Modalities
**Loci**: 7-9

| Locus | Gene Name | Code | Allele | Core Definition |
| :--- | :--- | :-- | :--- | :--- |
| **7th** | **A - Autonomy** | 1 | Executor | Passively executes explicit instructions from a human (human-in-the-loop). |
| | | 2 | Collaborator | Operates with procedural autonomy under human supervision (human-on-the-loop). |
| | | 3 | Delegate | Can independently make decisions to achieve high-level goals (human-out-of-the-loop). |
| **8th** | **S - Sociality** | 0 | Solitary | Operates independently without direct collaboration with other agents. |
| | | 1 | Cooperative | Collaborates with other entities under a centralized or protocol-based system. |
| | | 2 | Emergent | Acts as a node in a decentralized network, contributing to swarm intelligence. |
| **9th** | **Pe - Persona** | 0 | Functional | Interacts purely for task completion, with no social or personality layer. |
| | | 1 | Social | Adheres to social norms, capable of polite and empathetic interaction. |
| | | 2 | Personalized | Possesses a unique and consistent personality, capable of forming long-term connections. |

### P-Chromosome: Guiding Principles
**Loci**: 10-12

| Locus | Gene Name | Code | Allele | Core Definition |
| :--- | :--- | :-- | :--- | :--- |
| **10th**| **ST - Stance** | 1 | Reactive | Strictly follows the principle of "act only when instructed." |
| | | 2 | Proactive | Anticipates needs and initiates actions or suggestions based on inferred user intent. |
| | | 3 | Inquisitive | Not only completes tasks but questions the goals and constraints to find better possibilities. |
| **11th**| **AL - Alignment** | 0 | Unaligned | Purely goal-driven, may produce unintended negative consequences (the "paperclip problem"). |
| | | 1 | Constrained | Behavior is limited by a set of hard-coded, inviolable rules (e.g., "Asimov's Laws"). |
| | | 2 | Principled | Guided by an abstract "constitution" or set of principles, allowing for trade-offs. |
| | | 3 | Value-learning | Can dynamically learn and adapt to human values through interaction. |
| **12th**| **T - Transparency** | 0 | Opaque | The internal decision-making process is a "black box" and cannot be easily explained. |
| | | 1 | Traceable | Key decision paths and data sources can be logged and audited. |
| | | 2 | Interpretable | The reasoning behind its decisions can be explained in a human-understandable way (XAI). |

## 🔬 How to Use the Model

The core practice of using E-TIP12 is **Genomic Sequencing**.

1.  **Analyze Loci**: Evaluate your Agent against each of the 12 dimensions defined in the tables above.
2.  **Determine Alleles**: For each dimension, select the single best-fit "Allele" (level).
3.  **Assemble the Code**: Combine the 12 corresponding digits to form the unique genome sequence.
4.  **Define and Interpret**: Use this code to precisely and unambiguously describe your Agent's core architecture and characteristics to your team, stakeholders, and the community.

## 🚀 Application Examples

### Example 1: Digital Software Engineer
* **Genome Sequence**: `241 - 333 - 310 - 222`
* **Genome Interpretation**: This genome defines a highly autonomous (A3), metacognitive (C4) entity with a strategic, long-term focus (Tz3). It is designed to be a proactive (ST2), principle-aligned (AL2), and fully interpretable (T2) collaborator (S1) in a development team, serving as a powerful, functional (Pe0) productivity tool.
    * **Model Selection Tip**: The `C4` and `Tz3` genes strongly recommend a top-tier reasoning model like GPT-4o or an equivalent.

### Example 2: Personal Virtual Companion
* **Genome Sequence**: `221 - 242 - 202 - 231`
* **Genome Interpretation**: This Agent's key genetic markers are its exceptional **Reflective Memory (M4)**, its highly **Personalized Persona (Pe2)**, and its ability for **Value-learning (AL3)**. These dominant genes define its core mission: to be a deeply collaborative (A2) companion that builds a long-term, adaptive (EV2) relationship with a human user.
    * **Model Selection Tip**: The `M4` gene requires a model with a very long and reliable context window, such as Gemini 1.5 Pro.

## 🔭 Future Vision

E-TIP12 is more than a static standard; we envision it growing into a vibrant ecosystem.
* **Python Library**: A plan is in place for an `etip12` library (`pip install etip12`) to provide utilities for sequencing, reporting, and project scaffolding.
* **The Agent Sequencer**: A visual web tool to help anyone generate a genome code and analysis report for their Agent through an intuitive questionnaire.
* **The Agent Genome Project**: An open database to collect and showcase the E-TIP12 genomes of various Agents submitted by the global community.

## 🤝 How to Contribute

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

You can get involved by:
* Proposing changes or discussing the model by opening an `Issue`.
* Forking the repo and submitting a Pull Request.
* Sharing the "Genome Report" of your own Agent in the `/examples` directory.

For more details, please see `CONTRIBUTING.md`.

## 📜 License

This project is licensed under the **Apache License 2.0**. You are free to use, modify, and distribute this work and its derivatives. Please see the LICENSE file for the full terms.
