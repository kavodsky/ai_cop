# Statistical Foundations for Genomics & GWAS

A structured, self-contained learning resource for data and IT professionals who want to understand the statistical methods behind genome-wide association studies (GWAS) and polygenic risk scores (PRS).

No prior biology or genetics knowledge required. Basic Python and familiarity with descriptive statistics assumed.

---

## Who this is for

- Data scientists and analysts working in pharma or biotech
- IT professionals supporting genomic research projects
- Anyone who reads GWAS papers and wants to understand what the numbers actually mean

---

## Repository structure

```
genomics-stats/
│
├── module_01_confidence_intervals.ipynb
├── module_02_pvalue_multiple_testing.ipynb
├── module_03_regression.ipynb
├── module_04_genomics_fundamentals.ipynb
├── module_05_gwas_methodology.ipynb
├── module_06_prs_from_scratch.ipynb
│
└── README.md
```

---

## Modules

### ✅ Module 1 — Confidence Intervals
**Status:** complete

- What a confidence interval is and what it is not
- Building CI from scratch using the t-distribution
- How sample size controls CI width — the 1/√n relationship
- Odds Ratio (OR) and its CI — the core language of GWAS results
- Reading a forest plot: effect sizes the way papers present them

---

### 🔜 Module 2 — p-value and Multiple Testing
**Status:** in progress

- What a p-value actually means
- Why testing 1,000,000 SNPs simultaneously breaks the standard p < 0.05 threshold
- Bonferroni correction from scratch
- Why the GWAS threshold is p < 5×10⁻⁸ and not some other number

---

### 📋 Planned modules

| Module | Topic | Key concepts |
|--------|-------|--------------|
| 3 | Regression | Linear, logistic, covariates, effect size |
| 4 | Genomics fundamentals | DNA, SNP, allele, genotype, Hardy-Weinberg equilibrium |
| 5 | GWAS methodology | Study design, quality control, population stratification, PCA |
| 6 | Polygenic Risk Score | GWAS summary statistics, LD clumping, PRSice-2, model evaluation |

---

## Capstone project

All modules build toward one integrative project:

**Polygenic Risk Score for Coronary Heart Disease**

Using public GWAS summary statistics (CARDIoGRAMplusC4D), we build a PRS pipeline from scratch and evaluate its predictive performance against the classical Framingham Risk Score using ROC curves, AUC, and calibration plots.

The project is fully reproducible — every step from raw summary statistics to final evaluation is documented and commented.

---

## How to run

```bash
git clone https://github.com/yourorg/genomics-stats
cd genomics-stats
pip install numpy pandas matplotlib scipy
jupyter lab
```

All notebooks are self-contained. No external data downloads required for Modules 1–5.

---

## Design principles

Each module follows the same structure:

1. **Motivation** — why this concept matters in a real GWAS context
2. **Intuition** — simulation or visual before any formula
3. **Implementation** — code from first principles, every line commented
4. **Interpretation** — how this appears in actual research papers
5. **Exercises** — with one exercise that bridges to the next module

---

## Key references

**Statistics**
- StatQuest with Josh Starmer (YouTube) — intuitive explanations of every concept covered here
- *Statistics* — Freedman, Pisani, Purves

**Genomics & GWAS**
- *Genomic Data Science Specialization* — Johns Hopkins / Coursera
- Bush & Moore (2012) — "Chapter 11: Genome-Wide Association Studies", PLOS Computational Biology (open access, good starting point)

**PRS**
- Privé et al. (2022) — LDpred2, the current standard method for PRS construction
- Lambert et al. (2021) — "Towards clinical utility of polygenic risk scores", Nature Reviews Genetics

**Public datasets used**
- CARDIoGRAMplusC4D — GWAS summary statistics for coronary artery disease
- 1000 Genomes Project — population genomics reference panel
