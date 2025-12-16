# Self‑Improving Agentic RAG System

A **Self‑Improving Agentic RAG (Retrieval‑Augmented Generation) System** that extends traditional RAG pipelines with **autonomous reasoning agents**, **multi‑dimensional evaluation**, and an **evolution loop** that continuously refines its own decision‑making strategies.

This repository is a **from‑scratch, hand‑typed implementation** inspired by the article:

> *Building a Self‑Improving Agentic RAG System* — Fareed Khan

The goal of this project is to demonstrate **agentic system design**, **LLM orchestration**, and **self‑optimization patterns** suitable for real‑world, enterprise‑grade GenAI applications.

---

## Table of Contents

* [Overview](#overview)
* [Why Agentic RAG?](#why-agentic-rag)
* [System Architecture](#system-architecture)
* [Key Features](#key-features)
* [Project Structure](#project-structure)
* [Installation](#installation)
* [Quick Start](#quick-start)
* [How the Self‑Improvement Loop Works](#how-the-self-improvement-loop-works)
* [Evaluation Strategy](#evaluation-strategy)
* [Example Use Cases](#example-use-cases)
* [Limitations & Future Work](#limitations--future-work)
* [Credits & References](#credits--references)
* [License](#license)

---

## Overview

Traditional RAG systems retrieve documents and pass them to an LLM for generation. This project goes a step further by introducing:

* **Specialist agents** that reason about planning, execution, evaluation, and diagnosis
* **Multi‑objective evaluation** instead of single‑score grading
* **An evolution engine** that modifies system SOPs based on observed weaknesses

The result is a pipeline that can **analyze its own failures and iteratively improve its behavior**.

---

## Why Agentic RAG?

Classic RAG pipelines are:

* Static
* Hard‑coded
* Fragile when requirements change

Agentic RAG introduces:

* Decision‑making agents instead of linear chains
* Adaptive retrieval and reasoning strategies
* Feedback‑driven improvement loops

This architecture is especially useful for **complex enterprise workflows**, **research assistance**, and **high‑stakes reasoning tasks** where correctness and trade‑offs matter.

---

## System Architecture

At a high level, the system is composed of:

1. **Knowledge Infrastructure**
   Document ingestion, chunking, embedding, and indexing for retrieval.

2. **Agent Guild (Specialist Agents)**
   Independent agents responsible for planning, analysis, execution, evaluation, and diagnosis.

3. **Orchestration Layer**
   Coordinates agent interactions and manages execution flow.

4. **Multi‑Dimensional Evaluator**
   Scores outputs across multiple criteria (e.g., accuracy, clarity, feasibility).

5. **Evolution Engine**
   Proposes and tests improved SOPs based on evaluation feedback.

6. **Pareto Analyzer**
   Identifies optimal strategies across competing objectives.

---

## Key Features

* Agent‑based RAG architecture
* Modular, extensible agent design
* Multi‑objective evaluation framework
* Automated diagnosis of weak responses
* SOP evolution and strategy refinement
* Pareto‑front based optimization

---

## Project Structure

```text
.
├── agents/              # Specialist agents (planner, evaluator, diagnostician, etc.)
├── core/                # Orchestration and execution logic
├── evaluation/          # Scoring, metrics, and Pareto analysis
├── knowledge/           # Ingestion, embeddings, and retrieval
├── utils/               # Helper utilities
├── experiments/         # Iterative runs and evolution experiments
├── requirements.txt
└── README.md
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/<your-username>/autonomous-agentic-rag.git
cd autonomous-agentic-rag
```

Create and activate a virtual environment:

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Create a `.env` file for API keys:

```text
OPENAI_API_KEY=your_api_key_here
```

---

## Quick Start

Run the main workflow or notebook:

```bash
python main.py
```

or

```bash
jupyter notebook
```

Typical execution flow:

1. Ingest and index documents
2. Initialize agent guild
3. Process a user query
4. Evaluate generated responses
5. Trigger evolution loop if needed
6. Visualize performance trade‑offs

---

## How the Self‑Improvement Loop Works

1. **Generation** – Agents retrieve context and generate an answer
2. **Evaluation** – Output is scored across multiple dimensions
3. **Diagnosis** – Weaknesses are identified (e.g., shallow reasoning, hallucination)
4. **Evolution** – SOP Architect proposes modified agent strategies
5. **Re‑Execution** – New strategies are tested and compared
6. **Selection** – Pareto‑optimal strategies are retained

This loop allows the system to **learn structurally**, not just probabilistically.

---

## Evaluation Strategy

Instead of a single score, responses are evaluated using:

* Accuracy / factual correctness
* Reasoning depth
* Clarity and structure
* Cost and efficiency
* Constraint compliance

Results are analyzed using **multi‑objective optimization**, enabling principled trade‑off decisions rather than arbitrary tuning.

---

## Example Use Cases

* Research assistance with evolving reasoning strategies
* Enterprise knowledge assistants
* Policy and compliance analysis
* Technical documentation synthesis
* Multi‑step analytical decision support

---

## Limitations & Future Work

* Currently relies on LLM‑based evaluators
* No persistent long‑term memory across runs
* Limited automated benchmarking

Planned improvements:

* Human‑in‑the‑loop feedback
* Long‑term strategy memory
* Tool‑calling agents
* Domain‑specific evaluators
* Production‑grade monitoring

---

## Credits & References

* Fareed Khan — *Building a Self‑Improving Agentic RAG System*
* LangChain / Agentic AI design patterns
* Research on multi‑objective optimization and Pareto fronts

This repository is intended for **educational, research, and portfolio demonstration purposes**.

---

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
