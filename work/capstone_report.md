# Capstone Report — Lane 4: CTR / Engagement Opportunity Scoring

- **Author:** Ahmad
- **Lane:** Lane 4 — CTR / Engagement Opportunity Scoring
- **Repo:** https://github.com/widadfatimakhan/flyrank-internship-ml
- **Date:** 2026-08-23

> **The full report is the deployed research paper:**
> **https://widadfatimakhan.github.io/flyrank-internship-ml/**
>
> Every section of `capstone_report_template.md` is carried there rather than duplicated here,
> so the numbers can never drift between two copies. This file is the map.

## Where each rubric section lives

| Template section | In the deployed paper | Notebook that produced it |
|---|---|---|
| 0. Abstract | §1 Abstract | `capstone.ipynb` |
| 1. Problem framing | §2 Introduction and problem statement | `w01_research_question.ipynb`, `w02_ml_task_framing.ipynb` |
| 2. Data safety | §3 Data — exclusions, leakage risks, public-safety pass | `w03_data_contract.ipynb`, `w03_feature_leakage_check.ipynb` |
| 3. Baseline | §5 Results — frozen Week-4 rule row | `w04_baseline_score.ipynb` |
| 4. Model / analysis | §4 Methodology — features, label, method choice | `w05_model.ipynb` |
| 5. Evaluation | §4.5 Validation, §5 Results, §5 "Where the model is wrong" | `w05_model.ipynb`, `w06_validation_audit.ipynb` |
| 6. Interpretation | §5 "What the model leans on", §6 Limitations | `w04_signal_audit.ipynb`, `w05_model.ipynb` |
| 7. Recommendation | §7 Ranked recommendations — four actions with guardrails | `w07_action_playbook.ipynb` |
| 8. Reproducibility | §8 Reproducibility — seeds, environment, result-to-notebook map | all |
| 9. Acknowledgments & data credit | §9 — links to https://flyrank.ai | — |

## Headline, in the required claim language

**Observed** on 60,942 pages across 34 client portfolios, a Random Forest fitted on
February→March and applied unchanged to March→April **measured** precision@50 of 0.96 against
a frozen rule baseline at 0.90 and a **base rate of 0.095**; the K=200 margin held a 95%
bootstrap interval of +0.055 to +0.155, excluding zero. The improvement is **directional**,
not uniform — per-client AUC ranged 0.600 to 0.990, and one deployment window is not a
backtest. The queue is **decision-support** for which pages an editor opens first: it does not
diagnose what is wrong with a page, and no result here shows that editing one changes its
outcome.

## Sealed-evaluation note

The template asks that a sealed evaluation be checkable rather than taken on faith. **June 2026
was never read.** What is committed instead is the next-best thing: the time-forward test in
`w06_validation_audit.ipynb`, where the model was fitted on February→March and applied to
March→April without refitting, plus its metrics in
`work/outputs/ml09_validation_audit_receipts.json`. Two notebooks assert their reproduction
against a committed receipt before doing anything else and stop if it fails.

## Receipts

`work/outputs/` holds seven metrics JSONs (ML-04 through ML-10). Every number in the deployed
paper traces to one of them via the result-to-notebook map in §8.