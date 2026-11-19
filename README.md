# Hi, I'm Pavitra 👋

Final-year dual-degree student at **BITS Pilani** (B.E. Mechanical + M.Sc. Chemistry, 2027), interning in Client Success & Program Delivery at **Goodera**, Bengaluru.

**I measure things that run in production** — processes, models and growth systems — with guardrails, evaluation and the failure modes written down. Most of what follows carries a finding that reversed my own first conclusion.

📫 f20220970@pilani.bits-pilani.ac.in · [LinkedIn](https://www.linkedin.com/in/pavitra-seth-824540310)

---

## Operations, risk and controls

| Project | Links | What it found |
| --- | --- | --- |
| **process-transformation-lab** | [Code](https://github.com/f20220970-debug/process-transformation-lab) · [Results](https://f20220970-debug.github.io/process-transformation-lab/) | Process mining on a real 1,434-case workflow. One transition held **31% of all queue time** — the obvious fix. But the clock decomposes to **intake 38%, logged workflow 9%, closure 52%**, so that bottleneck was worth **1.8 days of 59**. Recommended instrumenting the unmeasured windows first. |
| **card-portfolio-risk** | [Code](https://github.com/f20220970-debug/card-portfolio-risk) · [Results](https://f20220970-debug.github.io/card-portfolio-risk/) | SQL risk profiling of **30,000 real card accounts** (180,000 account-months): roll rates, concentration, lead time, 6-sheet Excel model. A status field coded inconsistently across months made the book look like free fall; the comparable definition read as recovery. **Both were the coding.** |
| **bread-credit-mlops** | [Code](https://github.com/f20220970-debug/bread-credit-mlops) · [Results](https://f20220970-debug.github.io/bread-credit-mlops/) | Model validation with promotion gates. Blocked a candidate that ranked fine and was **wrong by 12.5 points on calibration**. My own serving monitor missed a stuck upstream feature until it watched inputs as well as outputs: **3/4 → 4/4** faults caught, zero false alerts. |
| **sc-transaction-monitoring** | [Code](https://github.com/f20220970-debug/sc-transaction-monitoring) · [Results](https://f20220970-debug.github.io/sc-transaction-monitoring/) | Fraud detection scored by **alert budget**, not accuracy (99.83% by flagging nothing) on 284,807 real card transactions. Predicted risk was **24× overstated** before recalibration. |
| **ozi-kids-qcommerce-analytics** | [Code](https://github.com/f20220970-debug/ozi-kids-qcommerce-analytics) · [Results](https://f20220970-debug.github.io/ozi-kids-qcommerce-analytics/) | 11 SQL analyses on **99K real orders**. At equal delivery time, a missed promise lifts 1–2★ reviews from **8.8% to 25.3%** — promise-kept beats speed as the KPI. Caught a NULL bug reporting 72% repeat rate against a true **1.9%**. |
| finance-recon-controls | [Code](https://github.com/f20220970-debug/finance-recon-controls) | Reconciliation controls over finance operations. |
| credit-risk-model-monitoring | [Code](https://github.com/f20220970-debug/credit-risk-model-monitoring) | Scorecard performance, population stability and drift tracked over time, with the thresholds that should trigger a model review. |
| evaratus-fde-lab | [Code](https://github.com/f20220970-debug/evaratus-fde-lab) | Field-level extraction evaluation on 2,000 noisy invoices: exposed a **19.4%** document pass rate hiding behind a healthy-looking accuracy number, tracked to 99.8%. |

## Agents and experimentation

| Project | Links | Highlight |
| --- | --- | --- |
| **chaos-liveops-agent** | [Code](https://github.com/f20220970-debug/chaos-liveops-agent) · [Daily eval](https://f20220970-debug.github.io/chaos-liveops-agent/) | Tunes a simulated puzzle game's difficulty: A/B tests each change, ships or rolls back inside retention and revenue guardrails, logs every decision. Re-evaluated **daily** on GitHub Actions. |
| **llm-triage-agent** | [Code](https://github.com/f20220970-debug/llm-triage-agent) · [Daily eval](https://f20220970-debug.github.io/llm-triage-agent/) | Claims guardrail → Gemini → local fallback → confidence router. On unseen wording, **20% → 72%** accuracy vs the local model. Refuses to publish when the LLM fails. |
| game-ua-budget-agent | [Code](https://github.com/f20220970-debug/game-ua-budget-agent) | Thompson sampling on predicted D30 player value: **+10.6%** revenue vs even split; caught a bidding incident in one day. |
| retention-uplift-engine | [Code](https://github.com/f20220970-debug/retention-uplift-engine) | Uplift targeting **113 vs 69** extra orders per 1,000 against churn-risk targeting; Kaplan–Meier; propensity-matched loyalty ROI. |
| marketplace-pricing-experiments | [Code](https://github.com/f20220970-debug/marketplace-pricing-experiments) | Switchback carryover bias (**37%**), elasticity with clustered SEs, CUPED (**−87%** variance), constrained price optimiser. |
| dynamic-pricing-bandits | [Code](https://github.com/f20220970-debug/dynamic-pricing-bandits) | Shared-model Thompson sampling: **98.4%** of oracle, 60% less regret than an A/B test. |
| dispatch-matching-sim | [Code](https://github.com/f20220970-debug/dispatch-matching-sim) | Hungarian batching plus forecast-led repositioning lifted fulfilment **63.6% → 83.5% on the same 80 drivers** (3-seed mean). Separately, a fleet-sizing test reached an **80% service level with 80 drivers against 160** under greedy dispatch (single seed), at **114 empty km per driver per day**. |

## Engineering

| Project | Links | Highlight |
| --- | --- | --- |
| **xr-3d-automation-pipeline** | [Code](https://github.com/f20220970-debug/xr-3d-automation-pipeline) · [Results](https://f20220970-debug.github.io/xr-3d-automation-pipeline/) | Mesh cleanup, unit detection and ML-driven LOD generation over real CAD assets: full-engine processing **179s → 52s**; **31%** fewer triangles than a fixed ratio. Found two validation defects in my own pipeline, including a glTF export mis-scaling an asset **1000×**. |
| distributed-rl-rollouts | [Code](https://github.com/f20220970-debug/distributed-rl-rollouts) | Shared-memory actor–learner system: **1.9× throughput on 2 cores**, worker recovery under 0.1s, and a measurement of the 30% of rollouts a strict on-policy learner would discard. |
| container-terminal-rl | [Code](https://github.com/f20220970-debug/container-terminal-rl) | PPO written from scratch on a terminal-dispatch environment: matched or beat the best of four rules in **all six scenarios**, **+7%** on an unseen six-crane layout. |
| call-insights-api | [Code](https://github.com/f20220970-debug/call-insights-api) | Queue-backed FastAPI service — Redis, MongoDB, retries, dead-letter, schema-validated JSON: **94%** intent accuracy vs a 62% keyword baseline on 50 synthetic calls labelled before testing. |
| trip-data-pipeline | [Code](https://github.com/f20220970-debug/trip-data-pipeline) | ETL over **5.97M** trips. |

## Business, growth and finance

| Project | Links | Highlight |
| --- | --- | --- |
| **india-agri-carbon-market** | [Code](https://github.com/f20220970-debug/india-agri-carbon-market) · [Results](https://f20220970-debug.github.io/india-agri-carbon-market/) | Sized India's agri carbon-removal opportunity on a 44.16 Mha rice base. A cross-check against published farmer earnings **broke my own model**: a flat 50/50 split implied a developer share of **−105% to 41%** for rice methane — the credit is worth less than the payment it must fund. Screening six real programmes then broke two more assumptions, in opposite directions. |
| **kaho-genz-growth** | [Code](https://github.com/f20220970-debug/kaho-genz-growth) · [Results](https://f20220970-debug.github.io/kaho-genz-growth/) | Positioning and acquisition arithmetic for a consumer app. The cheapest channel costs **3.2× less per install and 57% more per paying user**, and breakeven sits **13% above** the disclosed conversion rate — so the first move is sign-up drop-off (**17.6% of CAC**, no media spend), not more installs. |
| **hyderabad-housing-analytics** | [Code](https://github.com/f20220970-debug/hyderabad-housing-analytics) | Price prediction on **2,464 real listings** across 238 localities: gradient boosting at **6% median error (R² 0.91)** against 10% for regression, which I kept as the interpretable benchmark. Clustered 41 localities into 5 segments and named the thin-supply premium pockets. |
| **ev-market-sizing** | [Code](https://github.com/f20220970-debug/ev-market-sizing) | India E2W aftermarket sized bottom-up from Vahan data: **₹870 Cr FY26 → ₹5,600 Cr FY31** base case. Spend per vehicle moves FY31 by ₹2,200–3,000 Cr against ₹800–1,600 Cr for sales growth — so the lever is share of wallet, not market growth. Excel model CI-tested against a Python re-implementation. |
| soma-growth-console | [Code](https://github.com/f20220970-debug/soma-growth-console) · [App](https://soma-growth-console-ctm3kxywkrrytky4rbgrxr.streamlit.app/) | Founder planning tool: move growth levers and watch ARR, cash runway and Monte Carlo risk update. |
| arr-growth-model | [Code](https://github.com/f20220970-debug/arr-growth-model) | 24-month ARR and cash model in live Excel, matched to a Python implementation; Monte Carlo. |
| revenue-pipeline-forecaster | [Code](https://github.com/f20220970-debug/revenue-pipeline-forecaster) | Deal-level Monte Carlo within **3.8%** against 83% error for stage-weighted CRM forecasts. |
| soma-brokerage-ops-lab | [Code](https://github.com/f20220970-debug/soma-brokerage-ops-lab) · [Memo](https://github.com/f20220970-debug/soma-brokerage-ops-lab/blob/main/docs/Soma_Founders_Office_Memo.pdf) | Insurance brokerage operations: speed-to-lead, carrier routing, renewals, AI triage evaluation. |
| porter-category-growth-lab | [Code](https://github.com/f20220970-debug/porter-category-growth-lab) | Pricing × fulfilment, partner acquisition and M1 retention, driver-support redesign. |
| qcommerce-retention-sql | [Code](https://github.com/f20220970-debug/qcommerce-retention-sql) | 9 SQL analyses on **3.35M** Instacart orders, growth experiments, teardown. |
| noon-funnel-growth | [Code](https://github.com/f20220970-debug/noon-funnel-growth) | Funnel analysis and growth experiments. |
| eurekaforbes-service-insights | [Code](https://github.com/f20220970-debug/eurekaforbes-service-insights) | Service analytics case study. |
| nobroker-strategy-case | [Code](https://github.com/f20220970-debug/nobroker-strategy-case) | A **34× spread** in modelled value per lead by journey — and ranking the same journeys by conversion rate inverts the order, so the metric a growth team reaches for first points at the lowest-value one. Rewrote my own FY24 recommendation after the company's FY26 revenue mix outdated it. |
| lng-configuration-screener | [Code](https://github.com/f20220970-debug/lng-configuration-screener) | Techno-economic screen of four LNG liquefaction configurations against four customer types: levelized cost of liquefaction, scenarios and sensitivities in live Excel. |

<sub>Every repo states what its data is. Projects on real public datasets say which one; projects on simulated data say so and show method rather than company facts. Where a result rests on a single run or a small sample, the README says that too.</sub>

**Tools:** Python · SQL (CTEs, window functions) · pandas/NumPy/scikit-learn · Excel · FastAPI · Redis · Docker · GitHub Actions CI · pytest · Streamlit · Gemini API · Claude Code
