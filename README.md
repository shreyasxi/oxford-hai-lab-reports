# Research Reports — Oxford HAI Lab

**Shreyas Urgunde** · Predoctoral Research Assistant · Human Algorithm Interaction (HAI) Lab · Saïd Business School, University of Oxford

---

These reports document empirical research conducted at the HAI Lab, University of Oxford, from March to June 2026. The work spans two research projects: on foreign firms' China strategy and hybrid talent hiring, plus a structured predoc training programme on AI and labour markets.

---

## Reports at a Glance

| # | Report | Date | Supervisor |
|---|--------|------|------------|
| W1 | <a href="https://shreyasxi.github.io/oxford-hai-lab-reports/Urgunde_Week1_Report.pdf" target="_blank" rel="noopener noreferrer">CEO Sentiment and Strategic Stance of Foreign Firms Toward China</a> | Mar 2026 | Prof. Kejia Hu |
| W2 | <a href="https://shreyasxi.github.io/oxford-hai-lab-reports/Urgunde_Week2_Report.pdf" target="_blank" rel="noopener noreferrer">Financial and Market-Level Drivers of Foreign Firms' China Strategy</a> | Mar 2026 | Prof. Kejia Hu |
| W3 | <a href="https://shreyasxi.github.io/oxford-hai-lab-reports/W3_Replication_Report.pdf" target="_blank" rel="noopener noreferrer">Replication: Digital Transformation Pathway — Hiring Strategy for Business and Data Specialists</a> | Apr 2026 | Prof. Zhenzhen Jia |
| W4 | <a href="https://shreyasxi.github.io/oxford-hai-lab-reports/W4_robustness_report.pdf" target="_blank" rel="noopener noreferrer">Hiring Strategy and Firm Performance: Threshold Sensitivity, Model-Free Evidence, and Robustness Checks</a> | May 2026 | Prof. Zhenzhen Jia |
| W5 | <a href="https://shreyasxi.github.io/oxford-hai-lab-reports/W5_causal_validation_report.pdf" target="_blank" rel="noopener noreferrer">Robustness Checks and Causal Validation for Hybrid Talent Strategy Analysis</a> | May 2026 | Prof. Zhenzhen Jia |
| W6 | <a href="https://shreyasxi.github.io/oxford-hai-lab-reports/W6_main_specification_report.pdf" target="_blank" rel="noopener noreferrer">Main Empirical Specification: Hybrid Talent Strategy and Firm Performance</a> | Jun 2026 | Prof. Zhenzhen Jia |
| P1 | <a href="https://shreyasxi.github.io/oxford-hai-lab-reports/predoc_report_week1.pdf" target="_blank" rel="noopener noreferrer">Who Will AI Displace? Structural Barriers, Demand Traps, and the Limits of Early Evidence</a> | Apr 2026 | Prof. Kejia Hu |
| P2 | <a href="https://shreyasxi.github.io/oxford-hai-lab-reports/predoc_report_week2.pdf" target="_blank" rel="noopener noreferrer">Occupational Downgrading and Task Unbundling in High-Exposure AI Labor Markets</a> | May 2026 | Prof. Kejia Hu |
| P3 | <a href="https://shreyasxi.github.io/oxford-hai-lab-reports/predoc_report_week3.pdf" target="_blank" rel="noopener noreferrer">Does AI Adoption Cause Occupational Downgrading?</a> | Jun 2026 | Prof. Kejia Hu |

---

## Project 1 · Foreign Firms' China Strategy (Weeks 1–2)

**Supervisor:** Professor Kejia Hu, Founding Director, HAI Lab, University of Oxford

This project builds a longitudinal dataset on how nine multinational firms across healthcare, automotive, and information technology positioned themselves toward China from 2015 to 2025.

### Week 1 — CEO Sentiment and Strategic Stance

<a href="https://shreyasxi.github.io/oxford-hai-lab-reports/Urgunde_Week1_Report.pdf" target="_blank" rel="noopener noreferrer">`Urgunde_Week1_Report.pdf`</a>

I coded 175 executive statements from earnings calls, investor presentations, and annual reports on a five-point ordinal scale, *Committed Expansion* (1) to *Strategic Retreat* (5), using an LLM-assisted scheme validated at Krippendorff's α = 0.931. The central finding: strategic posture varies by **policy exposure type**, not sector. Firms subject to US semiconductor export controls (NVIDIA) undergo reactive, forced sentiment shifts. Healthcare and automotive firms show anticipatory, stable positioning despite comparable geopolitical pressure. The overall mean stance score across all nine firms remained at 2.09, firmly in *Optimistic Engagement* territory, throughout a decade of escalating US-China tension.

| Statistic | Value |
|-----------|-------|
| Executive statements coded | 175 |
| Multinational firms | 9 |
| Industry sectors | 3 (Healthcare, Automotive, Technology) |
| Years of coverage | 11 (2015–2025) |
| Intercoder reliability (α) | 0.931 |

### Week 2 — Financial and Market-Level Drivers

<a href="https://shreyasxi.github.io/oxford-hai-lab-reports/Urgunde_Week2_Report.pdf" target="_blank" rel="noopener noreferrer">`Urgunde_Week2_Report.pdf`</a>

Rather than measuring what executives say, this report measures what firms *do*. I construct a firm-year panel with 99 observations and 30 variables, coding 67 observable strategic events. Four ordered logit specifications test whether rhetoric, financial characteristics, and regulatory exposure predict observable strategic behaviour.

CEO stance score is a statistically significant predictor of observable China strategy outcomes (β = −1.46, p < 0.01): each one-point increase in cautious rhetoric is associated with a 77% reduction in the odds of expansion. US export controls are the only policy variable with significant predictive power (β = −3.88, p < 0.05). Financial variables (revenue, CapEx, ROE, leverage) show no significant association with strategic outcomes, suggesting that multinational China strategy in this period was shaped by regulatory feasibility and managerial framing rather than balance sheet characteristics.

| Metric | Value |
|--------|-------|
| CEO stance β (ordered logit) | −1.46\*\*\* |
| Export controls β | −3.88\*\* |
| Pseudo R² (4 specifications) | 0.20–0.23 |
| Outcome split (Expand / Maintain / Retreat) | 54% / 40% / 6% |
| Kruskal-Wallis H (stance vs. outcome) | 11.89, p = 0.003 |
| OLS robustness R² | 0.309 |

---

## Project 2 · Hybrid Talent Strategy and Firm Performance (Weeks 3–6)

**Supervisor:** Professor Zhenzhen Jia, School of Management, Xi'an Jiaotong University (XJTU) / HAI Lab

This four-week project replicates and extends Jia et al. (2025) on whether the *direction* of hybrid talent acquisition, specifically embedding data skills into business-facing roles (Hybrid B) versus overlaying business skills onto data roles (Hybrid D), predicts firm-level ROA. The dataset covers S&P 500 firms from 2011 to 2019, drawn from Lightcast job posting data.

### Week 3 — Replication

<a href="https://shreyasxi.github.io/oxford-hai-lab-reports/W3_Replication_Report.pdf" target="_blank" rel="noopener noreferrer">`W3_Replication_Report.pdf`</a>

Using OLS fixed-effects regressions (`pyfixest.feols`) with HC1 standard errors and industry and year fixed effects, I recover the Hybrid B ROA premium of +0.215–0.273 log-points, significant at 1% across all four specifications. Pure data specialist hiring (Pure D) generates no measurable ROA benefit. The *direction* of hybridity, not mere hybrid presence, drives financial value creation.

| Statistic | Value |
|-----------|-------|
| Firm-year observations | 3,367 |
| Hybrid B coefficient (Col. 4, persistent) | +0.273\*\*\* |
| Pure D coefficient (Col. 4) | −0.112 |
| Adjusted R² (Col. 4) | 0.319 |

### Week 4 — Threshold Sensitivity and Robustness

<a href="https://shreyasxi.github.io/oxford-hai-lab-reports/W4_robustness_report.pdf" target="_blank" rel="noopener noreferrer">`W4_robustness_report.pdf`</a>

Threshold sensitivity analysis confirms τ = 20% as the preferred specification: the b-ratio is bounded at [0, 0.66] with median ≈ 0.12, thresholds above 40% yield very few Hybrid B observations. Seven robustness checks (alternative thresholds, propensity-score-matched controls, rank-composition controls, skill-type decomposition) confirm the premium. Model-free evidence shows Hybrid B firms exhibit higher and less dispersed ROA distributions, with strategy adoption growing monotonically from 2011 to 2019.

| Metric | Value |
|--------|-------|
| Hybrid B ROA premium (τ = 20%) | +0.227\*\*\* |
| Significance range (τ = 15%–20% only) | +0.134\*\*\*–0.227\*\*\* |
| b-ratio in sample: range / median | [0, 0.66] / 0.12 |
| Adj. R² (preferred specification) | 0.317 |
| Trad. ML Hybrid B coefficient | +0.222\*\*\* (240 firm-years) |
| PSM matched Hybrid B pairs | 62 of 62 |

### Week 5 — Causal Validation

<a href="https://shreyasxi.github.io/oxford-hai-lab-reports/W5_causal_validation_report.pdf" target="_blank" rel="noopener noreferrer">`W5_causal_validation_report.pdf`</a>

After conditioning on firm fixed effects, the Hybrid B coefficient falls to +0.030 (s.e. 0.049, p > 0.5) and remains statistically indistinguishable from zero across every alternative specification, matching design, staggered-DiD estimator, and performance measure tested. Thirteen robustness and causal validation tasks converge: the cross-sectional premium documented in Week 3–4 is best interpreted as a **between-firm selection effect**: firms that adopt Hybrid B differ on unobserved pre-adoption characteristics that also predict higher ROA, rather than a causal return to hybrid hiring.

| Metric | Value |
|--------|-------|
| Hybrid B β under firm FE | +0.030 (s.e. 0.049, p > 0.5) |
| PSM avg. post-treatment effect (1:1) | −0.002 |
| Persistent adopters avg. post-ROA (N = 39) | −0.174 |
| Sun–Abraham / Callaway–Sant'Anna DiD | −0.090 / −0.050 |
| Cross-sectional premium (industry+year FE) | +0.219–0.227\*\*\* |
| Shift-share IV first-stage F | < 1 (weak instrument) |

### Week 6 — Main Specification

<a href="https://shreyasxi.github.io/oxford-hai-lab-reports/W6_main_specification_report.pdf" target="_blank" rel="noopener noreferrer">`W6_main_specification_report.pdf`</a>

The main specification synthesises all prior work. At τ_HB = 0.20 and τ_HD = 0.50, Hybrid B firms earn ROA 22.7% higher than otherwise-similar Pure B firms (β = +0.227, s.e. 0.051), matching the manuscript's Panel A coefficient exactly. The estimate is stable across six robustness tables. An event study documents significant positive pre-trends two-to-four years before adoption, confirming the selection interpretation: the result is a robust **conditional association**, not a clean causal effect.

| Statistic | Value |
|-----------|-------|
| Strategy firm-years | 4,281 |
| Regression sample | 3,367 |
| Hybrid B ROA premium | +22.7% |
| Threshold (τ_HB / τ_HD) | 0.20 / 0.50 |
| Robustness tables | 6 |

---

## Predoc Training Series · AI and Labour Markets (Weeks 1–3)

**Supervisor:** Professor Kejia Hu, Founding Director, HAI Lab, University of Oxford

A structured predoctoral training programme running alongside the main research projects, focused on AI-driven labour market disruption.

### Predoc Week 1 — Who Will AI Displace?

<a href="https://shreyasxi.github.io/oxford-hai-lab-reports/predoc_report_week1.pdf" target="_blank" rel="noopener noreferrer">`predoc_report_week1.pdf`</a>

A synthesis of two concurrent working papers: Massenkoff and McCrory (Anthropic, 2026) and Hemenway Falk and Tsoukalas (Penn/BU, 2026). Both converge on a counter-intuitive finding: the primary barrier to AI-driven labour displacement is not technical capability but **structural economic contradictions**. The Anthropic paper provides early empirical evidence of a shift hitting highly educated, well-paid workers disproportionately. The Penn/BU paper proves formally that competitive firms will rationally over-automate into a Pareto-inferior equilibrium that only a Pigouvian automation tax can correct. The report identifies a policy timing problem: the evidence required to justify intervention may arrive only after the displacement trap has already closed.

### Predoc Week 2 — Research Question Formulation

<a href="https://shreyasxi.github.io/oxford-hai-lab-reports/predoc_report_week2.pdf" target="_blank" rel="noopener noreferrer">`predoc_report_week2.pdf`</a>

Formulates an original research question on **occupational downgrading and task unbundling** in high-exposure AI labour markets. Situates the question within the Acemoglu-Restrepo (2020) task-based framework and the emerging literature on credential-occupation mismatch, arguing that aggregate unemployment statistics conceal occupational downgrading as the primary adjustment channel.

### Predoc Week 3 — Research Design

<a href="https://shreyasxi.github.io/oxford-hai-lab-reports/predoc_report_week3.pdf" target="_blank" rel="noopener noreferrer">`predoc_report_week3.pdf`</a>

Proposes a full empirical research design to test whether AI adoption causes occupational downgrading, using credential-occupation mismatch in high-exposure knowledge work as the primary outcome. Revised in response to Prof. Hu's feedback to narrow to a single core mechanism: the causal link between AI exposure and credential-occupation mismatch as occupational downgrading's most tractable empirical signature.

---

## About

These reports were prepared as part of a predoctoral research assistantship at the [Human Algorithm Interaction (HAI) Lab](https://www.sbs.ox.ac.uk/), Saïd Business School, University of Oxford (March–June 2026).

**Author:** Shreyas Urgunde · [shreyasxi.github.io](https://shreyasxi.github.io) · shreyas.urgunde@warwick.ac.uk

---

> **Note:** The underlying code and proprietary datasets used in this research are the intellectual property of the Human Algorithm Interaction (HAI) Lab, University of Oxford, and are not available for public distribution.
