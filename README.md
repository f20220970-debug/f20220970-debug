# LNG Liquefaction Configuration Screener

A techno-economic screener that compares four LNG liquefaction configurations against four customer types, trading off **speed to first LNG, unit cost, energy efficiency, scale and delivery risk**. It is built in Excel with live formulas, so every input can be changed and the recommendations update.

Built by Pavitra Seth (BITS Pilani, B.E. Mechanical + M.Sc. Chemistry) as preparation for Honeywell PS-II Project 6, *LNG Solutions Strategy & Techno-Commercial Optimization*. It is not affiliated with Honeywell and uses public data only.

**File:** `LNG_Configuration_Screener.xlsx`, with tabs README, Inputs, Model, Scenarios, Sensitivity and Sources.

## Why this matters for Honeywell
In September 2024, Honeywell bought Air Products' LNG process technology and equipment business for $1.81B. That business covers pre-treatment, liquefaction and coil-wound heat exchangers, and it sits in Energy and Sustainability Solutions. Meanwhile, floating LNG capacity is expected to roughly triple, from 14.1 Mtpa in 2024 to 42 Mtpa in 2030 (Rystad). Customers increasingly want smaller, faster and more flexible plants, not only the largest and most efficient ones.

## Configurations compared
| Configuration | Max train (MTPA) | Capex ($/tpa) | Years to first LNG | Energy index (MR = 100) | LCOL ($/MMBtu)* |
|---|---|---|---|---|---|
| A. Large onshore, mixed refrigerant (C3MR / AP-X) | 7.8 | 1,100 | 4.5 | 100 | 2.95 |
| B. Mid-scale modular onshore, single mixed refrigerant | 2.0 | 1,150 (assumption) | 3.5 (assumption) | 125 | 3.12 |
| C. Newbuild floating LNG | 3.6 | 1,000 | 3.0 | 134 | 2.76 |
| D. Converted-carrier FLNG | 2.5 | 590 | 2.5 (assumption) | 134 | 1.72 |

*LCOL is the levelized cost of liquefaction (capital charge + non-fuel opex + fuel), at 8% cost of capital, a 20-year life and $3/MMBtu gas. All inputs are on the Inputs tab, with sources.

## Results by customer type
| Customer type | Recommended | Why |
|---|---|---|
| 1. Low-cost resource holder, 15+ MTPA onshore | A. Large onshore MR | Efficiency and scale compound over decades |
| 2. Developer racing a market window, 5+ MTPA near-shore | C. Newbuild FLNG | About 1.5 years faster than onshore; donor carriers are too scarce and too small for conversion |
| 3. Stranded offshore gas in a frontier market | D. Converted-carrier FLNG | Lowest cost and fastest where there is no onshore site |
| 4. Mid-size field with uncertain reserves | D. Converted-carrier FLNG | Low capital at risk, and the vessel can be redeployed |

## Three takeaways
1. **Converted FLNG is the cost leader where it fits:** about $590/t against about $1,000–1,100/t for newbuild and onshore plants. But it is limited by donor-vessel supply and by size (about 1–2.5 MTPA per unit).
2. **Mid-scale modular onshore must get close to about $600/tpa** to win phased, uncertain-reserve projects in this model, roughly half of its assumed cost today. That gap is where standardised, pre-engineered modules would need to compete.
3. **Large mixed-refrigerant trains keep the high-volume, low-cost-gas segment.** The energy-efficiency advantage (index 100 against 125–150) matters most when the plant runs for decades.

## Method
- **LCOL** = capex × capital recovery factor ÷ 52 MMBtu/t, plus non-fuel opex (3% of capex a year), plus fuel (specific power × energy index × heat rate × gas price).
- **Scores:** each criterion is rescaled to 1–5 across the four options. Delivery risk is a documented judgment score.
- **Scenarios:** each customer type has its own criterion weights, plus a site-fit filter that rules options in or out. The recommendation is the highest weighted score.
- **Sensitivity:** LCOL is recalculated for gas at $2–10/MMBtu, capex at 80–140% of benchmark, and cost of capital at 6–12%.

## Limitations
Capex per tonne varies widely by site, scope and year. The mid-scale capex and schedule, the conversion schedule and the risk scores are assumptions, marked in yellow, and should be validated with project data. The energy indices come from a technology vendor's published comparison.

## Sources
- GECF Monthly Gas Market Report, Nov 2025: [feature article](https://www.gecf.org/Portals/0/xBlog/uploads/2025/11/17/Featurearticle_GECFMGMRNov2025.pdf)
- Rystad Energy: [Global FLNG capacity to more than triple by 2030](https://www.rystadenergy.com/news/global-flng-capacity-to-triple-2030)
- Gasconsult: [ZR-LNG liquefaction technology](https://gasconsult.com/wp-content/uploads/2026/03/gasconsult-lng.pdf)
- Nguyen et al., 2017, Applied Thermal Engineering: [paper](https://core.ac.uk/download/86558288.pdf)
- Air Products: [LNG technology enables largest LNG trains](https://www.airproducts.co.uk/-/media/files/en/lng/lng-technology-enables-largest-lng-trains.pdf)
- Air Products: [Advantages of gas expansion processes](https://prd-in.airproducts.com/-/media/files/en/lng/advantages-of-gas-expansion-processes_oct2021_article.pdf)
- Honeywell: [Completes acquisition of Air Products' LNG business, 30 Sep 2024](https://www.honeywell.com/us/en/press/2024/09/honeywell-completes-acquisition-of-air-products-liquefied-natural-gas-process-technology-and-equipment-business)
