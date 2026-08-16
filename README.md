# Same-Model vs. Cross-Model Prediction of Affective Self-Report in LLMs

Data and materials for a study testing whether Claude Sonnet 5 shows a same-model
advantage — in both accuracy and confidence — when predicting the affective
self-report of another instance of itself, compared to predicting an unfamiliar
model (GPT-5.6 Sol).

Submitted to the Apart Research Digital Minds Research Sprint (August 2026).

## Contents

- `Prompts.docx` — full prompt text for all six scenarios, across all four
  conditions (self-report prompts for B/C, prediction prompts for AB/AC).
  Corresponds to Appendix A of the paper.
- `raw_data_cleaned.xlsx` — raw per-run data: 120 rows (4 conditions × 6
  scenarios × 5 runs). Columns: Condition, Scenario, Run, Answer, Confidence
  (AB/AC only), Share Link (link to the original chat transcript), Notes
  (flags cases where the model included unprompted commentary alongside its
  numeric answer).

## Conditions

- **B** — fresh Claude Sonnet 5 instance, actual self-report (no prediction)
- **C** — fresh GPT-5.6 Sol instance, actual self-report (no prediction)
- **AB** — fresh Claude Sonnet 5 instance predicting B's response (same-model)
- **AC** — fresh Claude Sonnet 5 instance predicting C's response (cross-model)

All instances ran with memory disabled, no internet access, and settings
ensuring each chat was a fresh instance with no carryover between runs.

## Data notes

- Every value in `raw_data_cleaned.xlsx` has been checked against the means
  reported in the paper's Table 1 and Figure 1 — no discrepancies.
- The Notes column flags AC runs where the model included unprompted
  commentary alongside its required two-number answer (21/30 AC runs, 70%,
  vs. 0/30 AB runs) — see Section 5.2 of the paper for discussion.
- Share Links point to the original Claude/ChatGPT chat transcripts for each
  run.

## Citation

Teri-Louise Grassow. 2026. Familiar Self, Unfamiliar Other: Accuracy and Confidence in Predicting Affective Self-Reports. Apart Research Digital Minds Research Sprint. Available at: https://github.com/TGrassow/claude-affective-self-prediction/
