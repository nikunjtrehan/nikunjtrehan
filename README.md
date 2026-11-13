# Nikunj Trehan

**Applied AI · Payment workflows · Operating systems**

COBS student at Thapar Institute of Engineering and Technology. My projects span computer vision, payment-failure recovery, and RISC-V operating-system extensions.

[Remnant X demo](https://youtu.be/w_baW3A8f0M) · [Engineering decisions](https://nikunjtrehan.github.io/remnant-x/engineering-decisions/) · [RecoverAI overview](https://nikunjtrehan.github.io/recover-ai/)

## Selected projects

### [Remnant X](https://github.com/nikunjtrehan/remnant-x)
**Photographed offcuts → reviewed geometry → cutting plans**

Built for the Meta AI hackathon. Combines Meta SAM perception, model-assisted order interpretation, and deterministic geometry to plan parts across sheet remnants while preserving existing holes.

- **Engineering:** calibrated photo intake, hole-aware multi-sheet nesting, independent G-code checks, and operator-confirmed inventory updates.
- **Evidence:** a recorded demonstration plans ten custom parts across two photographed metal remnants. Physical experiments and their measurement limits are documented separately.
- **Scope:** a supervised prototype; real-machine cutting has not been demonstrated.

`Python` `FastAPI` `React` `TypeScript` `Computer vision` `Computational geometry`

[Demo](https://youtu.be/w_baW3A8f0M) · [Architecture](https://github.com/nikunjtrehan/remnant-x/blob/main/ARCHITECTURE.md) · [Physical validation](https://github.com/nikunjtrehan/remnant-x/blob/main/docs/architecture/PHYSICAL_VALIDATION_20261030.md) · [Automated checks](https://github.com/nikunjtrehan/remnant-x/actions/workflows/checks.yml)

### [RecoverAI](https://github.com/nikunjtrehan/recover-ai)
**Payment-failure recovery with bounded actions and an audit trail**

Built for the Razorpay AI Buildathon's Revenue Recovery track. Classifies payment failures, selects recovery actions, and generates English, Hindi, and Hinglish messages. The default decision path uses rules; an optional offline AI script generates a message template from audit summaries.

- **Engineering:** allowed-action checks, suspicious-payment escalation, mock payment integration, and SQLite decision records.
- **Evidence:** tests cover routing, guardrails, messaging, audit records, and mock recovery flows. The evaluation script explicitly simulates recovery outcomes.
- **Scope:** a hackathon prototype; simulated recovery figures are not merchant revenue or production results.

`Python` `FastAPI` `SQLite` `Streamlit` `Razorpay SDK`

[Project overview](https://nikunjtrehan.github.io/recover-ai/) · [Source and setup](https://github.com/nikunjtrehan/recover-ai#setup) · [Tests](https://github.com/nikunjtrehan/recover-ai/blob/main/tests/test_core.py) · [Evaluation](https://github.com/nikunjtrehan/recover-ai/blob/main/run_evaluation.py)

### [xv6 Plus](https://github.com/nikunjtrehan/os_project_xv6_plus)
**Memory management, threads, and debugging on RISC-V xv6**

A team project extending MIT's xv6 with lazy allocation, copy-on-write fork, paging policies, kernel threads, futex synchronization, tracing, signals, and an in-guest debugger.

- **My contribution record:** [merged integration PR](https://github.com/AkshitMishra1107/os_project_xv6_plus/pull/2) connecting tracing, signals, and debugging with the integrated kernel, plus regression checks and project documentation.
- **Evidence:** published full regression results and controlled comparisons of paging policies, COW tradeoffs, and equal-work parallel execution, with source checkpoints and raw captures.
- **Scope:** paging is validated on one CPU; the three-CPU configuration disables eviction. Results describe the documented QEMU configurations.

`C` `RISC-V` `Virtual memory` `Concurrency` `Kernel debugging`

[Architecture](https://github.com/nikunjtrehan/os_project_xv6_plus/blob/main/docs/architecture.md) · [Validation and comparisons](https://github.com/nikunjtrehan/os_project_xv6_plus/blob/main/docs/results/validation-upgrade/README.md) · [Reproduce the tests](https://github.com/nikunjtrehan/os_project_xv6_plus/blob/main/tools/README.md) · [Team repository](https://github.com/AkshitMishra1107/os_project_xv6_plus)

## Technical work to explore

| Area | Implementation and evidence |
| --- | --- |
| AI with explicit verification | [Remnant X: model roles, geometry, and final checks](https://nikunjtrehan.github.io/remnant-x/engineering-decisions/) |
| Decisions that can be inspected | [RecoverAI: strategy selection](https://github.com/nikunjtrehan/recover-ai/blob/main/src/recovery_agent.py) and [audit storage](https://github.com/nikunjtrehan/recover-ai/blob/main/src/audit.py) |
| Systems tradeoffs | [xv6 Plus: read-only versus write-all COW, paging patterns, and parallel scaling](https://github.com/nikunjtrehan/os_project_xv6_plus/blob/main/docs/results/validation-upgrade/README.md) |
