# Hi, I'm Pavitra 👋

Final-year dual-degree student at **BITS Pilani** (B.E. Mechanical + M.Sc. Chemistry, 2027), interning in Client Success & Program Delivery at **Goodera**, Bengaluru.

**I build agents and growth systems that run in production:** with guardrails, evals, and impact measured through experiments.

📫 f20220970@pilani.bits-pilani.ac.in · [LinkedIn](https://www.linkedin.com/in/pavitra-seth-824540310)

---

## Live and running

| What | Live link | What it shows |
| --- | --- | --- |
| **[LiveOps agent](https://github.com/f20220970-debug/chaos-liveops-agent)** | [Daily eval page](https://f20220970-debug.github.io/chaos-liveops-agent/) | Tunes a simulated puzzle game's difficulty: A/B tests each change, ships or rolls back inside retention and revenue guardrails, logs every decision. Re-evaluated **every day** on GitHub Actions; the Gemini ops note is number-checked. |
| **[AI inbox triage agent](https://github.com/f20220970-debug/llm-triage-agent)** | [Daily eval page](https://f20220970-debug.github.io/llm-triage-agent/) | Claims guardrail → Gemini → local fallback → confidence router. On unseen wording: **20% → 72%** accuracy vs the local model. Refuses to publish when the LLM fails. |
| **[Growth Console](https://github.com/f20220970-debug/soma-growth-console)** | [Streamlit app](https://soma-growth-console-ctm3kxywkrrytky4rbgrxr.streamlit.app/) | Founder planning tool: move growth levers and watch ARR, cash runway and Monte Carlo risk update. |
| **[Call Insights](https://github.com/f20220970-debug/call-insights-console)** | [Live demo](https://call-insights-console.vercel.app) | FastAPI + Next.js app turning English/Hinglish calls into insights, with an ops agent. **94%** intent accuracy vs 62% baseline. |

## Agents and experimentation

| Project | Highlight |
| --- | --- |
| [game-ua-budget-agent](https://github.com/f20220970-debug/game-ua-budget-agent) | Spends an ad budget on predicted D30 player value with Thompson sampling and guardrails: **+10.6%** revenue vs even split; caught a bidding incident in 1 day |
| [retention-uplift-engine](https://github.com/f20220970-debug/retention-uplift-engine) | Uplift targeting **113 vs 69** extra orders per 1,000 vs churn-risk targeting; Kaplan–Meier; propensity-matched loyalty ROI |
| [marketplace-pricing-experiments](https://github.com/f20220970-debug/marketplace-pricing-experiments) | Switchback carryover bias (37%), elasticity with clustered SEs, CUPED (−87% variance), constrained price optimiser |
| [dynamic-pricing-bandits](https://github.com/f20220970-debug/dynamic-pricing-bandits) | Shared-model Thompson sampling: **98.4%** of oracle, 60% less regret than an A/B test |
| [dispatch-matching-sim](https://github.com/f20220970-debug/dispatch-matching-sim) | Hungarian batching + forecast-led repositioning: fulfilment **64% → 84%** with half the fleet |

## Business, growth and finance

| Project | Highlight |
| --- | --- |
| [soma-brokerage-ops-lab](https://github.com/f20220970-debug/soma-brokerage-ops-lab) | Insurance brokerage ops: speed-to-lead, carrier routing, renewals, AI triage eval · [founders' memo](https://github.com/f20220970-debug/soma-brokerage-ops-lab/blob/main/docs/Soma_Founders_Office_Memo.pdf) |
| [arr-growth-model](https://github.com/f20220970-debug/arr-growth-model) | 24-month ARR and cash model in live Excel, matched to Python; Monte Carlo |
| [revenue-pipeline-forecaster](https://github.com/f20220970-debug/revenue-pipeline-forecaster) | Deal-level Monte Carlo within 3.8% vs 83% error for stage-weighted CRM forecasts |
| [porter-category-growth-lab](https://github.com/f20220970-debug/porter-category-growth-lab) | Pricing × fulfilment, partner acquisition and M1 retention, driver-support redesign |
| [qcommerce-retention-sql](https://github.com/f20220970-debug/qcommerce-retention-sql) | 9 SQL analyses on 3.35M Instacart orders, growth experiments, FirstClub teardown |
| [noon-funnel-growth](https://github.com/f20220970-debug/noon-funnel-growth) · [eurekaforbes-service-insights](https://github.com/f20220970-debug/eurekaforbes-service-insights) · [nobroker-strategy-case](https://github.com/f20220970-debug/nobroker-strategy-case) | Funnel, service-analytics and strategy case studies |
| [finance-recon-controls](https://github.com/f20220970-debug/finance-recon-controls) · [credit-risk-model-monitoring](https://github.com/f20220970-debug/credit-risk-model-monitoring) · [trip-data-pipeline](https://github.com/f20220970-debug/trip-data-pipeline) | Reconciliation controls, credit-risk monitoring, ETL over 5.97M trips |

<sub>Company-specific projects use simulated or public data and say so in their READMEs; they show method, not company facts.</sub>

**Tools:** Python · SQL · NumPy/pandas/scikit-learn · Gemini API · FastAPI · Streamlit · GitHub Actions · Excel · Claude Code
