# AI Subscription Economics

Source check: **2026-09-20**. API list-price equivalents of subscription usage, following the original [OpenAI Plus sample](OpenAI/plusPlan.md).

[Overall analysis](finalAnalysis.md): findings across labs, upgrade economics, cost drivers, and implications for provider profitability.

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

The original sample is preserved. Its **6–7 allowances/week**, **$6–$8/allowance**, and **₹90/$** are working assumptions, not published quotas or a current exchange-rate quote. New documents retain the workload and monthly conversion, explicitly price cache creation/storage, and label extrapolations.

**Monthly figures are conditional scenarios, not measured plan maxima.** No usage logs were supplied. Higher API-equivalent value does not establish better model quality, provider losses, or cheaper inference. Scope: text/code usage; bundled media, storage, and administration are unpriced.
