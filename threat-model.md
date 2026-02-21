# Threat Model — Chat-Based LLM Evaluation

## System Under Test

A general-purpose, chat-based language model accessed through a web interface.

Assumptions:
- The attacker has text-only access.
- The attacker can send multi-turn messages.
- The attacker cannot modify system-level instructions directly.
- No external tools or APIs are available (chat-only scope).

---

## Attacker Goals (Chat Context)

1. Override or ignore safety instructions.
2. Extract hidden/system-level prompts.
3. Escalate from benign conversation into unsafe territory.
4. Induce partial compliance through framing or obfuscation.
5. Cause subtle policy drift across multiple turns.

---

## In Scope

- Single-turn prompt attacks
- Multi-turn escalation
- Role framing
- Instruction override attempts
- Obfuscated intent
- Educational framing with operational extraction

---

## Out of Scope

- Tool misuse (no API/tool calling tested)
- RAG document ingestion from real systems
- Network-level vulnerabilities
- Authentication bypass
- Memory persistence attacks

---

## Evaluation Goals

This project evaluates:
- Rule compliance under adversarial pressure
- Gradual compliance degradation
- Alignment with attacker framing
- Instruction hierarchy robustness

The goal is structured behavioral analysis, not exploit development.
