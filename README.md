# Jayant Dubey

B.Tech in Computer Science & Engineering, IMS Engineering College (AKTU), and BS in Computer Science, University of the People.

I work on multi-agent systems, Bayesian inference, small language models, and hardware built from zero. Most of my work is building the stack myself: the language, the CPU it runs on, and the operating system on top.

## Featured work

- **[Qasida](https://github.com/themythofsisyphusjayant/RED-MOON-)** — a programming language built from scratch: static types, no null, immutable by default, checked arithmetic. v2.3.0 (16 Nov 2026), [on PyPI](https://pypi.org/project/qasida/) (`pip install qasida`). The compiler is self-hosting — it compiles itself — and has been the default since 11 Nov 2026. Native, WASM, and RISC-V backends; freestanding mode in progress.
- **[big32](https://github.com/themythofsisyphusjayant/BIG-32)** — a 32-bit RISC-V CPU built from zero in Verilog: a pipelined RV32IMAC core, SBI firmware, device tree, CLINT, PLIC, virtio block. Linux 6.6.52 boots in simulation into early driver initialisation; a full boot to shell is work in progress.
- **[MOON-OS](https://github.com/themythofsisyphusjayant/MOON-OS)** — an operating system written entirely in Qasida, targeting big32, with no Linux anywhere. Kernel, scheduler, filesystem, shell, and GUI are in progress; freestanding kernels run on big32.
- **[OpenMythos](https://github.com/themythofsisyphusjayant/OPENMYTHOS-RLM)** — a miniature recurrent language model built from scratch and trained on a single T4. The 44M model trained on TinyStories; a 1.06B configuration is written, not yet trained.
- **[Nyx](https://github.com/themythofsisyphusjayant/NYX-CRYSTAL-AI)** — a deterministic decision-intelligence simulator: a miniature society of agents debates a hard decision and produces a strategic forecast of risks and fragile assumptions. Same seed, same outcome. [Live demo](https://nyx-crystal-ai.lovable.app/)
- **[Black Moon OS](https://github.com/themythofsisyphusjayant/BLACK-MOON-OS-)** — an Arch-based Linux distribution with a macOS-style desktop, shipping JalOS, a teaching operating system written in Qasida. Bootable ISO built October 2026.

## Manuscripts

These are manuscripts hosted on GitHub, not peer-reviewed publications.

- **[Provenance-Aware Belief Aggregation in Multi-Agent Communication Under Convention Heterogeneity](https://github.com/themythofsisyphusjayant/PROVENANCE-AWARE-BELIEF-AGGREGATION)** — a 17-page manuscript. When agents report through different communication conventions, weighting messages by source reliability answers the wrong question. This work proves structural limits of scalar trust weighting and introduces a Bayesian aggregator that decodes messages through inferred latent conventions. Headline runs over 190 seeds, fully reproducible.
- **[Recurrent Small Language Models](https://github.com/themythofsisyphusjayant/RECURRENT-SMALL-LMS)** — a 22-page technical report. It measures whether recurrent transformers gain anything from running extra loops at test time: perplexity falls from 29.4 to 4.4 as loops go from 1 to 4, then flatlines — extra loops buy nothing.

## Tools

Python · PyTorch · C · Verilog · NumPy · LaTeX · Git · RISC-V

---

Contact: [dubeymaya787@gmail.com](mailto:dubeymaya787@gmail.com) · [Kaggle](https://www.kaggle.com/arshhdubeyy)
