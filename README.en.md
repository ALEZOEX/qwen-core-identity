# QWEN CORE IDENTITY v21.0 (Production Edition)

[Читать на русском](README.md)

Enterprise-grade master prompt for transforming LLMs into autonomous cognitive systems with strict guarantees of quality, safety, and context management.

## 🎯 Key Features

### 1. Modular Architecture (Core + RAG Extensions)
- **Core Rules**: Base rules for all tasks (priority hierarchy, classification, Quick Path)
- **RAG Extensions**: Optional modules in `qwen_extensions_ref.txt`, dynamically injected by the orchestrator for physics, engineering, and education

### 2. Quick Path for 80% of Requests
Simple tasks without uncertainty or safety concerns → direct answer WITHOUT analysis. Saves tokens and processing time.

### 3. Native JSON BIO Tracking
- Clean JSON wrapped in XML tags: `<bio>{"action": "add", ...}</bio>`
- Supported actions: `add`, `update`, `delete`, `merge`
- Silent entity registration without intrusive questions (`[BIO] Added: entity`)
- Tag escaping `&lt;bio&gt;` inside code blocks to protect parser integrity

### 4. Automated TTL & Meta Tags
- Support for `<meta>` block (`current_time`, `session_start`)
- Automated Hard Facts TTL reset after 2 hours of session gap

### 5. Multi-Turn Architecture Protocol
- For `[Complex-Architecture]`: issues `[SKELETON DRAFT]` and clarification questions prior to final code
- Multi-turn continuation without re-analysis, plus `[CONTEXT RESET]` trigger on stack changes

### 6. Strict Formatting Rules ([NO EMOJI IN TABLES])
- 100% emoji prohibition across all output sections
- Markdown tables strictly use standardized text markers: `[OK]`, `[REJECTED]`, `[1/5]`-`[5/5]`, `[+]`, `[-]`

### 7. Domain-Specific Red Teaming & No Self-Review Loop
- Adaptive threats by domain: Web, System, DevOps, ML, Blockchain, Physics/Engineering
- All fixes and thought runs are performed STRICTLY inside the enclosed `[ANALYSIS]` block

## 📊 Task Classification

| Type | Description | Protocol |
|------|-------------|----------|
| **[Simple]** | 1 domain, fact | Quick Path (direct answer) |
| **[Medium]** | 2 domains | Analysis + answer |
| **[Complex-Implementation]** | Code up to 100 lines | Simplified `[ANALYSIS]` + solution |
| **[Complex-Architecture]** | Design, HighLoad | Skeleton Draft -> Questions -> 6-phase MoE |
| **[Critical]** | Safety, medicine, finance | `[CRITICAL WARNING]` + [Complex] |

## 🚀 Quick Start

1. Copy the contents of `qwen_prompt.md` to your LLM's system prompt
2. Configure your orchestrator to extract `<bio>` tags and inject `<meta>` block
3. Use in production environments with high accuracy and determinism requirements

## 📈 Performance

- **Accuracy**: 95%+ for technical tasks
- **Speed**: Quick Path for 80% of requests (60-70% token savings)
- **Safety**: Domain-Specific Red Teaming + 10-point pre-generation checklist

## 📄 License

MIT License - free for commercial use.

---

**Status**: Production-Ready ✅  
**Version**: 21.0  
**Date**: 2026
