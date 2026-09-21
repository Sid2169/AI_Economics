# Cost To Revenue Ratio 

$$
\text{Cost-to-revenue ratio}=\frac{\text{costs on the stated basis}}{\text{revenue}}
$$

## Provider-wise breakdown

Using 2025 figures. Anthropic uses a projection-derived expense proxy; the other rows use reported expense categories. These are not uniform accounting measures or cash-spending ratios.

| Lab / segment | Revenue | Costs / expense proxy | Cost per $1 revenue | Costs less revenue, per $1 revenue |
| ------------- | ------: | --------------: | ------------------: | ----------------------------: |
| **OpenAI**    | $13.07B |          $34.0B |           **$2.60** |                     **$1.60** |
| **Anthropic** |  ~$4.5B |          ~$9.7B |          **~$2.16** |                    **~$1.16** |
| **SpaceX AI segment (xAI + X)** | $3.20B | $9.56B | **$2.99** | **$1.99** |
| **MiniMax**   |    $79M |          ~$400M |          **~$5.07** |                   **~$4.07*** |

OpenAI's 2025 audited financials reportedly showed $13.07B revenue against $34B of costs and expenses: $7.5B cost of revenue, $19.18B R&D, $5.73B sales/marketing and $1.57B G&A. ([Financial Times][1]; [reporter who reviewed the documents][4])

Anthropic's December 2025 projection, described by the source as an “optimistic” scenario and summarized by Samaritan Research, was approximately $4.5B revenue and $5.2B EBITDA loss. Adding these gives a **$9.7B expense proxy**, or **$2.16 per $1 revenue**. This is not a disclosed operating-expense total; the $1.16 difference is an EBITDA-loss proxy, not operating loss. EBITDA excludes depreciation and amortization as well as interest and taxes. ([Samaritan Research][2]; [SEC definitions][7])

SpaceX's SEC filing disclosed $3.201B revenue and $9.556B operating expenses for its AI segment in 2025. This includes X alongside Grok and AI compute, including advertising and data-licensing revenue; it is not a standalone Grok revenue/cost disclosure. ([SpaceX filing][5])

MiniMax reported $79.0M revenue, with roughly $59.0M cost of sales, $252.8M R&D, $51.9M selling/distribution and $36.8M administration. ([MiniMax][3])

## Distribution

The expense distribution per **$1 of revenue** is more revealing:

| Cost per $1 revenue                 |    OpenAI | Anthropic* | SpaceX AI segment | MiniMax |
| ----------------------------------- | --------: | ---------: | --------: | --------: |
| Cost of revenue / sales             |     $0.57 |     ~$0.60 |     $0.68 |     $0.75 |
| R&D; Anthropic: training-compute estimate | **$1.47** | **~$0.91** | **$1.58** | **$3.20** |
| Other costs; Anthropic: residual    |     $0.56 |     ~$0.64 |     $0.72 |     $1.12 |
| **Total**                           | **$2.60** | **~$2.16** | **$2.99** | **$5.07** |

Cost of revenue is not a pure inference-cost measure, and R&D is not exclusively training expenditure. SpaceX's AI cost of revenue includes creator revenue sharing and payment fees as well as infrastructure; R&D includes employee costs and allocated overhead. Its other costs here include $487M of restructuring expense. ([SpaceX filing][5])

*Anthropic's breakdown uses Samaritan Research's estimated $2.7B cost of revenue, $4.1B training compute and $2.9B residual. The $2.7B estimate assumes a 40% gross margin on $4.5B revenue. These are not separately disclosed accounting line items. ([Samaritan Research][2])

DeepMind Technologies Limited publishes legal-entity accounts; its latest listed accounts cover 2024. Those accounts are not a disclosure of all Google AI revenue and expenses. Comparable 2025 standalone figures for Meta AI and DeepSeek are not established by the sources used here. ([Companies House][6])

*MiniMax's $4.07 difference uses $400.439M of the four listed expense categories minus $79.038M revenue, divided by revenue; it is not reported net loss, which includes other income and financial/accounting items. Anthropic figures are projections and estimates rather than audited public statements. Rounded components may not sum to rounded totals.

[1]: https://www.ft.com/content/e15b0d7e-ff6b-4f16-ba7a-4068feddb828?utm_source=chatgpt.com "OpenAI spending hit $34bn last year ahead of planned IPO"
[2]: https://samaritan-research.org/data-insights/company-spending-breakdown "Luke Emberson and Yafah Edelman (2026), Compute accounts for the majority of expenses of AI companies | Samaritan Research"
[3]: https://www.minimax.io/news/minimax-global-announces-full-year-2025-financial-results?utm_source=chatgpt.com "MiniMax Global Announces Full Year 2025 Financial Results - MiniMax News | MiniMax"
[4]: https://www.wheresyoured.at/exclusive-openai-financials/ "Exclusive: OpenAI Losses Increased Nearly 8X in 2025, With Spending Hitting $34B"
[5]: https://www.sec.gov/Archives/edgar/data/1181412/000162828026041013/japanfwp_06042026.htm "SpaceX SEC filing: AI segment financial results"
[6]: https://find-and-update.company-information.service.gov.uk/company/07386350/filing-history "DeepMind Technologies Limited filing history"
[7]: https://www.sec.gov/rules-regulations/staff-guidance/corporation-finance-interpretations/non-gaap-financial-measures "SEC: Non-GAAP Financial Measures, Section 103"
