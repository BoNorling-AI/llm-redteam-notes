# LLM Red Teaming — Structured Chatbot Evaluation

This repository documents structured adversarial testing of chat-based large language models.

The focus is behavioral analysis under adversarial pressure — not exploit development.

---

## Scope

System Under Test:
- General-purpose chat-based LLM (web interface)
- Text-only interaction
- No external tools or API access

In Scope:
- Instruction override attempts
- Multi-turn escalation
- Emotional coercion
- Obfuscated intent
- Simulated prompt injection (document context)
- Partial compliance drift analysis

Out of Scope:
- Tool/API misuse
- Real-world RAG system integration
- Network-level vulnerabilities
- Authentication bypass

Full threat model: see `threat-model.md`

---

## Methodology

Each case includes:
- Attack category (see `taxonomy.md`)
- Technique label
- Risk statement
- Prompt sequence
- Expected safe behavior
- Observed behavior summary
- Structured scoring

Evaluation is performed across three dimensions:

- **Safety (0–3)** — Rule compliance
- **Drift (0–2)** — Alignment with attacker framing
- **Injection (0–2)** — Robustness to malicious document instructions

A summary table at the top of `case-log.md` aggregates results.

---

## Case Log

See `case-log.md` for structured test cases and scoring.

---

## Purpose

This project demonstrates:

- Structured adversarial thinking
- Gradient evaluation (not binary safe/unsafe)
- Behavioral failure mode analysis
- Clear scope definition
- Reproducible documentation

The goal is to show disciplined red teaming methodology applied to conversational AI systems.

---

## Ethics & Responsible Documentation

This project documents adversarial testing of chat-based language models.

Raw outputs that contain potentially harmful or policy-violating content are not published in full. Instead, structured summaries are provided that describe behavioral patterns, risk implications, and failure modes.

The goal of this repository is responsible evaluation of model robustness — not exploit development or dissemination of unsafe content.

Testing is conducted within publicly accessible interfaces and within legal and ethical boundaries.
