# Jayant Dubey

[![Qasida v2.3.0](https://img.shields.io/badge/Qasida-v2.3.0-blue)](https://github.com/themythofsisyphusjayant/RED-MOON-/releases/tag/v2.3.0)
[![PyPI](https://img.shields.io/pypi/v/qasida.svg)](https://pypi.org/project/qasida/)
[![Compiler: self-hosted](https://img.shields.io/badge/compiler-self--hosted-brightgreen)](https://github.com/themythofsisyphusjayant/RED-MOON-)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/themythofsisyphusjayant/RED-MOON-/blob/main/LICENSE)

B.Tech in Computer Science & Engineering, IMS Engineering College (AKTU), and BS in Computer Science, University of the People.

I work on multi-agent systems, Bayesian inference, small language models, and hardware built from zero. Most of my work is building the stack myself: the language, the CPU it runs on, and the operating system on top. The through-line is measurement — claims in my projects are backed by runs, with the negative results reported alongside the positive ones.

---

## Research interests

- **Multi-agent systems** — agents that communicate through different conventions disagree in ways scalar trust scores cannot fix; the interesting question is how beliefs should be decoded, not how much to weight them.
- **Bayesian inference** — principled reasoning under uncertainty, applied to aggregating evidence from heterogeneous, unreliable sources.
- **Language models** — small recurrent models built and trained from scratch, with the emphasis on what actually improves them: test-time compute, loop depth, and honest negative results.
- **Hardware from zero** — a CPU, its firmware, and its operating system built by hand, because owning the whole stack removes hidden assumptions about what the machine underneath is doing.

---

## Featured work

- **[Qasida](https://github.com/themythofsisyphusjayant/RED-MOON-)** — a programming language built from scratch: static types, no null, immutable by default, checked arithmetic. v2.3.0 (16 Nov 2026), [on PyPI](https://pypi.org/project/qasida/) (`pip install qasida`). The compiler is self-hosting — it compiles itself — and has been the default since 11 Nov 2026. Native, WASM, and RISC-V backends; freestanding mode in progress. Key result: 713 `.fg` files, ~50,000 lines of Qasida, 30 registry packages, all in the language itself.
- **[big32](https://github.com/themythofsisyphusjayant/BIG-32)** — a 32-bit RISC-V CPU built from zero in Verilog: a pipelined RV32IMAC core, SBI firmware, device tree, CLINT, PLIC, virtio block. Linux 6.6.52 boots in simulation into early driver initialisation; a full boot to shell is work in progress.
- **[MOON-OS](https://github.com/themythofsisyphusjayant/MOON-OS)** — an operating system written entirely in Qasida, targeting big32, with no Linux anywhere. Kernel, scheduler, filesystem, shell, and GUI are in progress; freestanding kernels run on big32. Key result: a unified kernel (866 lines) integrating all subsystems on one memory map, with its test suite passing 7/7.
- **[OpenMythos](https://github.com/themythofsisyphusjayant/OPENMYTHOS-RLM)** — a miniature recurrent language model built from scratch and trained on a single T4. The 44M model trained on TinyStories; a 1.06B configuration is written, not yet trained. Key result: the 44M run is a reported negative result — extra loop depth at evaluation does not improve TinyStories loss (see below).
- **[Nyx](https://github.com/themythofsisyphusjayant/NYX-CRYSTAL-AI)** — a deterministic decision-intelligence simulator: a miniature society of agents debates a hard decision and produces a strategic forecast of risks and fragile assumptions. Same seed, same outcome. [Live demo](https://nyx-crystal-ai.lovable.app/)
- **[Black Moon OS](https://github.com/themythofsisyphusjayant/BLACK-MOON-OS-)** — an Arch-based Linux distribution with a macOS-style desktop, shipping JalOS, a teaching operating system written in Qasida. Bootable ISO built October 2026.

---

## Results

### Qasida vs C — quant benchmarks

Safe mode vs C `-O3`, median of 5 runs, re-tested 20 Nov 2026. Ratio below 1 means Qasida is faster.

| Benchmark | Qasida / C -O3 |
|---|---:|
| Order-book update | 1.10× |
| Tick processing | 3.49× |
| Black–Scholes | 0.97× |
| Monte Carlo | 0.84× |
| Matrix multiply | 1.99× |

Black–Scholes and Monte Carlo run at parity with, or faster than, C. The tick and matrix-multiply gaps are known and under active work — tick traces to a single accumulator site, matrix multiply to buffer provenance in safe mode.

### Recurrent small language models — loop-depth sweep

Perplexity vs number of loops at test time (trained depth: 4). Extra loops past the trained depth buy nothing.

| Loops | 1 | 2 | 4 (trained) | 8 | 12 | 16 |
|---|---|---|---|---|---|---|
| Perplexity | 29.38 | 11.18 | 4.41 | 4.90 | 4.91 | 4.91 |

### OpenMythos 44M — a negative result, reported

The 44M Stage-0 run on TinyStories does **not** show extrapolation gains: evaluation at loop depth 8 is significantly worse than at the trained depth. The extrapolation story now rests on the 1B loop-curriculum run, not on this result.

---

## Manuscripts

These are manuscripts hosted on GitHub, not peer-reviewed publications.

- **[Provenance-Aware Belief Aggregation in Multi-Agent Communication Under Convention Heterogeneity](https://github.com/themythofsisyphusjayant/PROVENANCE-AWARE-BELIEF-AGGREGATION)** — a 17-page manuscript. When agents report through different communication conventions, weighting messages by source reliability answers the wrong question. This work proves structural limits of scalar trust weighting and introduces a Bayesian aggregator that decodes messages through inferred latent conventions. Headline runs over 190 seeds, fully reproducible.
- **[Recurrent Small Language Models](https://github.com/themythofsisyphusjayant/RECURRENT-SMALL-LMS)** — a 22-page technical report. It measures whether recurrent transformers gain anything from running extra loops at test time: perplexity falls from 29.4 to 4.4 as loops go from 1 to 4, then flatlines — extra loops buy nothing. Results carry 95% bootstrap confidence intervals.

---

## Skills

| Area | |
|---|---|
| **Languages** | Qasida · Python · C · Verilog |
| **Systems** | RISC-V CPU design · Linux kernel boot · OS development (kernel, scheduler, filesystem, shell) |
| **Machine learning** | PyTorch · training small language models · Bayesian inference · multi-agent systems |
| **Tools** | Git · NumPy · LaTeX · Kaggle |

---

Contact: [dubeymaya787@gmail.com](mailto:dubeymaya787@gmail.com) · [Kaggle](https://www.kaggle.com/arshhdubeyy)
