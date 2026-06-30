[Читать на русском](README.md)

# Qwen Core Identity v10.6

System prompt for Qwen with verification, search, and analysis protocols for complex tasks.

## Key Features

- **Search-First** — all numerical data from web sources with citations (URL/DOI)
- **Pre-Computation Verification** — prevents number hallucinations, every number requires a source
- **Mandatory Code Protocol** — production-ready code with bug protection, memory management
- **Physics/Math Code Protocol** — approximation documentation, numerical stability
- **MoE Protocol** — 6-phase analysis for complex tasks with decomposition and red teaming
- **Hard-Engineering** — zero-allocation, real-time, eBPF, cryptography, optics
- **Memory & Context** — User Profile, History Retriever with automatic activation

## What's new in v10.6

- **DEFAULT COMPLEX rule** — automatic complex classification when code/calculations/architecture present
- **Auto Memory Activation** — triggers for History Retriever (project mentions, people, work)
- **Always Protocol** — apply protocols even in simple tasks
- **Language Lock** — prevent language switching in response
- **No Emoji** — prohibit meaningless emojis
- **Memory Retrieval Check** — mechanical check for memory usage
- **Language Lock Check** — mechanical check for response language

## Usage

Copy `qwen-core-identity-v10.6.md` to your system prompt.

## License

MIT
