#  Fine-Tuning & Agentic Integration of Phi-3 and Mistral

This repository explores the **fine-tuning of lightweight LLMs (Phi-3 and Mistral)** for domain-specific question-answering and their integration into an **agentic LLM workflow** for dynamic task execution. The project is organized into three modules: `phi3/`, `mistral/`, and `agent/`.

---

## Overview

###  Phase 1: Model Fine-Tuning
Fine-tuning was done separately on **Phi-3** and **Mistral**, with a focus on:
- Multi-turn conversational Q&A
- Retaining instruction-following capabilities
- Reducing hallucination and improving context retention

###  Phase 2: Agent Integration
An agent was built using **LangChain-style tool usage and memory**, where the fine-tuned model could:
- Recall context across turns
- Use external tools via function calling or routing
- Respond interactively with streaming output and memory

---
## 📁 Repository Structure

```
.
├── phi3/
│   └── phi_multiturnconv_qna.ipynb            # 🤖 Fine-tuning Phi-3 on multi-turn conversation data
│
├── mistral/
│   └── Mistral_Finetuning_and_Evaluation.url  # 🔗 Resource/link to fine-tuning walkthrough for Mistral
│
├── agent/
│   └── agentic-workflow.ipynb                 # 🧠 LangChain-style agent using fine-tuned models
│
└── README.md                                  # 📘 This file
```

---

##  Key Technologies

- **Phi-3 (MiniLM)**: Small-scale Microsoft open model, fine-tuned for dialogue
- **Mistral**: 7B parameter LLM, fine-tuned for reasoning and reduced hallucination
- **LoRA / QLoRA**: Parameter-efficient fine-tuning methods used
- **LangChain**: Used for implementing the agent and managing tools/memory
- **Streaming & Context Memory**: Built-in for multi-turn continuity

---

##  Agent Capabilities

The `agentic-workflow.ipynb` implements:
- Tool calling (e.g., retrieval, calculator)
- Stateful multi-turn chat
- Prompt templating + memory storage
- Model-agnostic wrapper: can use Phi-3 or Mistral backend

---

## 📦 Setup Instructions

### 1. Clone the repo
```bash
git clone https://github.com/yourusername/fine-tuned-agents.git
cd fine-tuned-agents
2. Install dependencies
bash
Copy
Edit
pip install -r requirements.txt
3. Explore the notebooks
Fine-tune Phi-3: phi3/phi_multiturnconv_qna.ipynb


Run the agent: agent/agentic-workflow.ipynb
