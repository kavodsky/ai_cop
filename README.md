# AI in Pharma & Biotech — Research Notes

A personal research compendium at the intersection of AI, computational biology, and drug discovery.

The guiding question:

> *How do we extract meaningful biological signal from noisy, high-dimensional data — and turn it into actionable insight for medicine?*

This repository is organized around four deep concepts that underpin modern biomedical AI. Each research track is a practical exploration of one of these concepts, grounded in real biological data and problems.

---

## Four core concepts

**Uncertainty** — how to measure it, represent it, and make decisions under it.
Every experiment in medicine produces uncertain estimates. Understanding uncertainty — through statistics, Bayesian reasoning, and probabilistic modeling — is the foundation for everything else here.

**Dynamics** — how biological systems change over time.
Disease is not a snapshot. Gene expression, heart rhythm, drug response — all are dynamic processes. Time series analysis and signal processing are the tools for reasoning about biological dynamics.

**Causality** — the difference between correlation and cause.
Finding that a gene variant is associated with disease is not the same as understanding why. Moving from association to causal mechanism is what transforms a genomic signal into a drug target.

**Signal integration** — combining weak evidence into strong conclusions.
No single measurement tells the full story. Polygenic risk scores, multi-omics integration, and multimodal AI models are all answers to the same question: how do we combine many weak signals into something clinically useful?

---

## Research tracks

### `genomics-stats/` — Uncertainty
*Statistical foundations for genomic data analysis*

Building rigorous intuition for statistical inference — the language in which all genomic results are expressed.

| Module | Topic | Core concept |
|--------|-------|-------------|
| 01 | Confidence intervals | Quantifying uncertainty in effect estimates |
| 02 | p-value & multiple testing | Why GWAS uses p < 5×10⁻⁸ |
| 03 | Regression | Modeling relationships between genotype and phenotype |
| 04 | Bayesian inference & acquisition functions | From frequentist to probabilistic reasoning; Gaussian Processes in drug design |
| 05 | GWAS methodology | Genome-wide association from first principles |
| 06 | Polygenic Risk Score | Integrating thousands of small effects into a single predictor |

Capstone: end-to-end PRS pipeline for coronary heart disease using CARDIoGRAMplusC4D public data.

---

### `time-series/` — Dynamics *(coming Q3 2026)*
*Modeling biological processes that unfold over time*

Biological systems are dynamic. This track builds the tools to reason about change, rhythm, and temporal patterns in biomedical data.

| Module | Topic | Biological application |
|--------|-------|----------------------|
| 01 | Time series fundamentals | Stationarity, autocorrelation, decomposition |
| 02 | Heart rate variability (HRV) | Autonomic nervous system as a dynamic system |
| 03 | Mood & physiological signals | Predicting psychological state from cardiac rhythm |
| 04 | Forecasting models | ARIMA, Prophet, neural approaches |
| 05 | Survival analysis | Time-to-event modeling in clinical trials |

Data: PhysioNet open datasets (ECG, HRV), MIMIC-III clinical data.

---

### `signal-processing/` — Dynamics + Signal Integration *(coming Q3 2026)*
*Extracting structure from noisy biological measurements*

Every biological measurement is a signal embedded in noise. This track covers the mathematical tools for separating the two.

| Module | Topic | Biological application |
|--------|-------|----------------------|
| 01 | Fourier transform & frequency domain | Decomposing ECG into frequency components |
| 02 | Filtering & noise removal | Cleaning EEG and genomic signals |
| 03 | Wavelet analysis | Non-stationary signals — EEG, gene expression |
| 04 | Genomic signal processing | Chromosome as a discrete signal; LD structure |
| 05 | Deep learning for biosignals | CNN and transformer models for ECG classification |

---

### `causality-and-targets/` — Causality *(planned Q4 2026)*
*From genomic association to therapeutic hypothesis*

Association is not causation. This track covers the methods that bridge the two — and connects directly to how AI is used in modern drug target discovery.

| Module | Topic |
|--------|-------|
| 01 | Mendelian randomization | Using genetics as a natural experiment |
| 02 | Causal inference frameworks | DAGs, do-calculus, counterfactuals |
| 03 | Target identification with AI | How platforms like Variant Bio use genomic AI |
| 04 | Multi-omics integration | Combining genomics, transcriptomics, proteomics |

---

## How notebooks are structured

Every notebook follows the same pattern:

1. **Motivation** — the biological or clinical problem this method addresses
2. **Intuition** — simulation or visualization before any formula
3. **Implementation** — code from first principles, every line commented
4. **Interpretation** — how this appears in real research papers
5. **Exercise** — one open question that leads into the next module

Public datasets only. All analyses are fully reproducible.

---

## Progress

| Track | Concept | Status |
|-------|---------|--------|
| `genomics-stats` | Uncertainty | Active — Module 1 complete |
| `time-series` | Dynamics | Starting Q3 2026 |
| `signal-processing` | Dynamics + Integration | Starting Q3 2026 |
| `causality-and-targets` | Causality | Planned Q4 2026 |

---

## Selected references

**Foundations**
- Freedman, Pisani, Purves — *Statistics*
- MacKay — *Information Theory, Inference, and Learning Algorithms* (free online)

**Genomics**
- Tam et al. (2019) — "Benefits and limitations of genome-wide association studies", Nature Reviews Genetics
- Privé et al. (2022) — LDpred2, Bioinformatics

**Causality**
- Pearl & Mackenzie — *The Book of Why*
- Davey Smith & Hemani (2014) — Mendelian randomization, Nature Reviews Genetics

**Signal processing & time series**
- Oppenheim & Schafer — *Discrete-Time Signal Processing*
- PhysioNet — open biomedical signal datasets

**AI in drug discovery**
- Jumper et al. (2021) — AlphaFold2, Nature
- Ingraham et al. (2023) — protein language models, Nature
