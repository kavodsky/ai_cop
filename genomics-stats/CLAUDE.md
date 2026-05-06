# CLAUDE.md — genomics-stats

This track builds statistical foundations for genomic data analysis, progressing from basic inference to a full polygenic risk score pipeline.

## Learning progression

```
Confidence intervals
    ↓
p-value & multiple testing       ← current focus
    ↓
Regression (linear + logistic)
    ↓
Bayesian inference & acquisition functions
    ↓
GWAS methodology
    ↓
Polygenic Risk Score (capstone)
```

## What the user knows so far

- Confidence interval: what it means, how it is computed, why CI width depends on 1/√n
- Standard error: SE = s/√n, intuition for why it exists
- Odds Ratio: how to compute it, how to interpret it, why CI crossing 1.0 means non-significance
- Forest plot: how to read effect sizes and CIs in GWAS results
- SNP, allele, genotype: basic genomic vocabulary
- GWAS: the core logic — testing millions of SNPs for association with disease

## Key concepts in this track

**SNP** — a position in the genome where people differ by one letter (A, T, C, or G).

**Allele** — the specific letter at a SNP position. Two alleles per person (one from each parent).

**Genotype** — the combination of two alleles: AA, AG, or GG.

**GWAS** — genome-wide association study. Tests ~1 million SNPs simultaneously for association with a disease outcome. Uses logistic regression with OR as effect size.

**OR (Odds Ratio)** — effect size for binary outcomes. OR = 1.0 means no effect. OR > 1.0 means risk allele. OR < 1.0 means protective allele. A CI that crosses 1.0 means the result is not significant.

**PRS (Polygenic Risk Score)** — a weighted sum of thousands of SNP effects that predicts an individual's genetic risk for a disease.

**Multiple testing problem** — why GWAS uses p < 5×10⁻⁸ instead of p < 0.05. Testing 1 million SNPs simultaneously means ~50,000 false positives at p < 0.05 even with no real effects.

## Capstone project

End-to-end PRS pipeline for coronary heart disease:
- Data: CARDIoGRAMplusC4D GWAS summary statistics (public)
- Method: LD clumping + thresholding, then LDpred2
- Evaluation: compare PRS vs Framingham Risk Score using ROC, AUC, calibration plot

## How to help in this track

- Always connect statistical concepts to their GWAS application. If explaining p-value, show why it matters for SNP testing.
- Use the LDL cholesterol / coronary heart disease example consistently — it is the thread running through all modules.
- The user learns best through simulation and visualization. Suggest code when explaining a concept.
- When the user asks "why", answer at two levels: mathematical reason and biological intuition.
- Preferred datasets for exercises: 1000 Genomes Project, CARDIoGRAMplusC4D, PhysioNet (for later signal processing crossover).

## Common misconceptions to address

- "95% CI means 95% probability the true value is inside" — incorrect. The 95% refers to the procedure, not any single interval.
- "p-value is the probability the null hypothesis is true" — incorrect. It is the probability of observing data this extreme if the null were true.
- "A non-significant result means no effect" — incorrect. It means we cannot rule out no effect with the current sample size.
- "OR = 1.09 is always a small effect" — depends entirely on CI. OR = 1.09 with CI [1.07, 1.11] is a very precise, real finding.
