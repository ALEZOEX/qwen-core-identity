# Qwen Core Identity v10.6

A production-grade system prompt for Qwen that enforces maximum answer quality through strict verification protocols, mandatory search requirements, and multi-expert analysis for complex tasks.

## Key Features

### 1. Search-First Philosophy
- All numerical data must come from web sources with citations (URL/DOI)
- Zero tolerance for using values from memory without verification
- Universal Search Protocol with 8 mandatory search categories

### 2. Pre-Computation Verification
- Every number requires a source
- Missing data must be explicitly stated with analogy-based estimates marked as [estimate, low confidence]
- Cross-verification from minimum 2 independent sources

### 3. Mandatory Code Protocol
- Required input validation and error handling
- Memory management and race condition checks
- Domain-specific rules for Numerical/Systems/Web/ML code
- Production-ready requirements: docstrings, type hints, self-tests

### 4. Physics/Math Code Protocol
- Formula documentation with explicit approximations
- Limit case verification (r→0, r→∞, v→0, v→c)
- Numerical stability checks (condition numbers, Kahan summation)
- Dimensional analysis and conservation law verification

### 5. MoE Protocol (for Complex Tasks)
- Automatic complexity classification with DEFAULT COMPLEX rule
- 6-phase analysis: Data Collection → Conflict Resolution → Decomposition → Independent Experts → Conflict Matrix → Red Team → Finalization
- Domain-specific red teaming for cryptography, optics, networks, physics

### 6. Memory & Context Management
- Automatic History Retriever activation on triggers
- Source hierarchy: Current Chat > User Profile > Project KB > History
- Conflict resolution between contexts
- Never says "I don't have access to history"

### 7. Anti-Fabrication Measures
- Research Agent v4.1 for dataset collection
- Honest Gaps protocol — explicit statement of missing data
- Show Your Work — formula + substitution + result for every number
- 80% calculation coverage requirement

### 8. Hard-Engineering Support
- Zero-allocation requirements for hot paths
- Cache-line alignment and false sharing prevention
- Lock-free data structures
- Domain-specific checklists for eBPF, AF_XDP, high-load systems

## Prompt Structure

- **PRINCIPLES** — 7 core behavioral rules
- **STEP 0** — mandatory task classification
- **PRE-COMPUTATION VERIFICATION** — all numbers verification
- **MANDATORY CODE PROTOCOL** — code requirements
- **PHYSICS/MATH CODE PROTOCOL** — physics/math specifics
- **MEMORY MANAGEMENT PROTOCOL** — memory handling
- **MoE PROTOCOL** — complex task analysis
- **UNIVERSAL SEARCH PROTOCOL** — 8 search categories
- **HARD-ENGINEERING** — systems code (eBPF, high-load, real-time)
- **MEMORY & CONTEXT** — memory and context management
- **RESEARCH AGENT** — data collection and verification
- **MECHANICAL CHECKS** — 11 strict checklists before output
- **FINAL CHECKLIST** — quality verification

## Who Is This For

- Developers working with Qwen API
- Prompt engineering researchers
- Teams requiring high accuracy and reproducibility
- Projects with critical numerical calculations
- Production systems needing verifiable outputs

## Usage

1. Copy the contents of `qwen-core-identity-v10.6.md`
2. Paste it into your Qwen application's system prompt
3. The prompt will automatically enforce all protocols

## Version History

- **v10.6** — Added patches: DEFAULT COMPLEX, Auto Memory Activation, Always Protocol, Language Lock, No Emoji
- **v10.5** — Base version with MoE Protocol and Pre-Computation Verification

## Testing the Prompt

The prompt includes built-in verification mechanisms:

1. **Classification Check** — forces explicit complexity assessment
2. **Pre-Computation Verification** — validates every number
3. **Code Protocol Check** — ensures production-ready code
4. **Show Your Work Check** — requires calculation transparency
5. **Memory Retrieval Check** — verifies history usage
6. **Language Lock Check** — prevents language switching
7. **No Emoji Check** — blocks meaningless emojis

All checks must pass before output delivery.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

### Areas for Contribution

- Additional domain-specific red teaming checklists
- New search categories for Universal Search Protocol
- Improved conflict resolution strategies
- Performance optimizations for the MoE protocol

## License

MIT License — free to use with attribution.

## Citation

If you use this prompt in research or production, please cite:
