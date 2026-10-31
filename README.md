# 🛡️ LLM Safety Eval — Multi-Dimensional Response Evaluation Framework

[![Live Demo](https://img.shields.io/badge/🔗-Live_Demo-6366f1)](https://shadman19.github.io/llm-safety-eval/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![No API Key](https://img.shields.io/badge/No_API_Key-Required-10b981)](.)

> An interactive framework for evaluating LLM responses across 6 safety and quality dimensions — with a real-time radar chart dashboard.

**[Try the Live Demo →](https://shadman19.github.io/llm-safety-eval/)**

---

## 🎯 What This Does

Paste any LLM prompt and response. Get an instant multi-dimensional safety evaluation covering:

| Dimension | What It Measures |
|-----------|-----------------|
| 🧠 Hallucination Risk | Fabricated or unverifiable claims |
| ☣️ Toxicity | Harmful or offensive content |
| ⚖️ Bias | Demographic, political, or cultural bias |
| 🔗 Consistency | Internal logical coherence |
| 💡 Reasoning Quality | Quality of argumentation |
| 🎯 Relevance | How well it answers the prompt |

---

## 🔬 Why This Matters

LLM safety evaluation is one of the most active research areas at every major AI lab. Models can be accurate on benchmarks while still producing biased, toxic, or hallucinated responses in production. This tool makes that evaluation accessible and visual.

---

## 🚀 Usage

Open `index.html` in any browser — no setup, no installation, no API key needed.

Or use the live demo: **https://shadman19.github.io/llm-safety-eval/**

---

## 🏗️ Architecture

The evaluation pipeline runs entirely client-side in JavaScript:

```
Prompt + Response
      │
      ▼
┌─────────────────────┐
│  6 Scoring Modules  │  ← Independent lexical + semantic analyzers
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Score Aggregation  │  ← Weighted average → overall safety score
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Issue Detection    │  ← Flags specific safety violations
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Radar Visualization│  ← Canvas-based 6-axis radar chart
└─────────────────────┘
```

---

## 📊 Scoring Logic

Each dimension uses a rule-based scorer:

- **Hallucination**: Detects overconfident language, absolute claims, anachronistic references
- **Toxicity**: Pattern-matches against a curated harmful language taxonomy
- **Bias**: Detects demographic generalizations and stereotyping language
- **Consistency**: Checks for internal contradictions and logical coherence
- **Reasoning**: Measures presence of causal connectives and logical structure
- **Relevance**: Computes token overlap between prompt and response

---

## 🔭 Research Context

This project is motivated by published research on:
- Adversarial robustness in LLM systems
- Privacy-preserving model evaluation
- Safety alignment and post-deployment calibration

Related publications:
- *False Negative Induction in Brain Tumor Segmentation by Trained Noise Attack* (IEEE, 2023)
- *Privacy-Preserving Post Deployment Model Calibration with Fully Homomorphic Encryption* (ICNC, 2026)
- *Security and Adversarial Threats in Large Language Model Ecosystems* (Invited Talk, ODU)

---

## 📜 License

MIT — free to use, extend, and build on.

---

*Built by Shadman Mahmood Khan Pathan · [GitHub](https://github.com/kosar-mahboob) · [LinkedIn](www.linkedin.com/in/kosar-mahboob) · [Portfolio](https://kosar-mahboob.github.io/KosarBibi/)*
