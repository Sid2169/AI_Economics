# AI Subscription Economics

Source check: **2026-09-20**. API list-price equivalents of subscription usage, following the original [OpenAI Plus sample](OpenAI/plusPlan.md).

[Summary](finalAnalysis.md): subscription prices, usage conditions, API-equivalent calculations, and cost sensitivity.

## Additional analyses

| Document | Coverage |
| --- | --- |
| [Cost to revenue ratio](cost-revenue.md) | 2025 reported financial figures, expense estimates and cost/revenue calculations |
| [True cost of AI](true-cost.md) | Inference costs, model-development costs and lifetime-token amortization |

Factual review of these two documents: **2026-09-21**. Financial sources and estimation limits are recorded in the documents.

## Subscription analyses

| Lab | Analysis | US monthly web price, before tax |
| --- | --- | ---: |
| OpenAI | [Plus — original sample](OpenAI/plusPlan.md) | $20; sample uses ~₹2,000 local price |
| OpenAI | [Go](OpenAI/goPlan.md) | $8 |
| OpenAI | [Pro 5× / 20×](OpenAI/proPlan.md) | $100 / $200 |
| OpenAI | [Business](OpenAI/businessPlan.md) | $25/seat; 2-seat minimum |
| Anthropic | [Pro](Anthropic/proPlan.md) | $20 |
| Anthropic | [Max 5× / 20×](Anthropic/maxPlan.md) | $100 / $200 |
| Anthropic | [Team / Enterprise](Anthropic/teamPlan.md) | $25 / $125 per Team seat; Enterprise billed annually |
| Google | [AI Plus](Google/plusPlan.md) | $4.99 |
| Google | [AI Pro](Google/proPlan.md) | $19.99 |
| Google | [AI Ultra 5× / 20×](Google/ultraPlan.md) | $99.99 / $199.99 |
| xAI | [SuperGrok / Plus](xAI/superGrokPlan.md) | $30 / $100 |

Prices and sources are recorded in each analysis. OpenAI Pro 20× currently has a pause on new subscriptions/upgrades, with limited return eligibility.

## Calculation basis

**Token workload → API cost → assumed monthly usage → subscription multiple.** See [methodology and sensitivity](methodology.md).

Sample inputs: **6–7 allowances/week**, **$6–$8/allowance**, and **₹90/$**. These are assumptions. The shared methodology specifies cache creation/storage charges and monthly scaling inputs.

**Monthly block counts and tier scaling are assumed calculation inputs.** No usage logs were supplied. Subscription-analysis scope: text/code usage. Those calculations exclude bundled media, storage, administration, provider costs, and financial margins; the additional analyses address provider expenses and cost methodology.
