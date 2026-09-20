# AI Economics — Summary of Data and Calculations

As of **2026-09-20**. USD, before tax. Prices and API rates are sourced in the linked plan documents and [methodology](methodology.md).

## Calculation inputs

* One block: **3.95M tokens** — 3M cache reads, 0.7M ordinary input, 0.1M cache creation, 0.15M output/reasoning.
* Monthly input: **26–30 blocks**, with **28** as the reference calculation. These quantities originate from the sample assumption; no subscriber usage measurements are available.
* API-equivalent expenditure: **V = blocks × API cost/block**.
* Subscription ratio: **V / monthly subscription price**.
* API/subscription price equality: **monthly subscription price / API cost/block**.

## Base subscriptions

| Subscription / API comparator | Monthly price | API cost/block | API equivalent at 26–30 blocks | Ratio at 28 blocks | Price equality, blocks/month |
| --- | ---: | ---: | ---: | ---: | ---: |
| [ChatGPT Plus / GPT-5.6 Sol](OpenAI/plusPlan.md) | $20 | $7.50 | **$195–$225** | **10.50×** | 2.67 |
| [Claude Pro / Sonnet 5](Anthropic/proPlan.md) | $20 | $3.75 | **$97.50–$112.50** | **5.25×** | 5.33 |
| [Google AI Pro / Gemini 3.1 Pro Preview](Google/proPlan.md) | $19.99 | $4.45 | **$115.70–$133.50** | **6.23×** | 4.49 |
| [SuperGrok / Grok 4.6](xAI/superGrokPlan.md) | $30 | $4.00 | **$104–$120** | **3.73×** | 7.50 |

Plus uses the shared cache-write calculation and [$20 US price](https://learn.chatgpt.com/docs/pricing). The original sample uses a $6–$8 block-cost range and ~₹2,000 subscription price.

## Higher-tier calculations

The monthly block counts below are **assumed inputs**, not published token allowances. The 5× and 20× calculations multiply the 26–30-block baseline by 5 and 20 respectively.

| Plan / comparator | Monthly price | Assumed blocks/month | API equivalent/month | Ratio at 140 or 560 blocks |
| --- | ---: | ---: | ---: | ---: |
| [OpenAI Pro 5× / Sol](OpenAI/proPlan.md) | $100 | 130–150 | **$975–$1,125** | **10.50×** |
| [OpenAI Pro 20× / Sol](OpenAI/proPlan.md) | $200 | 520–600 | **$3,900–$4,500** | **21.00×** |
| [Claude Max 5× / Sonnet](Anthropic/maxPlan.md) | $100 | 130–150 | **$487.50–$562.50** | **5.25×** |
| [Claude Max 20× / Sonnet](Anthropic/maxPlan.md) | $200 | 520–600 | **$1,950–$2,250** | **10.50×** |
| [Google Ultra 5× / Gemini](Google/ultraPlan.md) | $99.99 | 130–150 | **$578.50–$667.50** | **6.23×** |
| [Google Ultra 20× / Gemini](Google/ultraPlan.md) | $199.99 | 520–600 | **$2,314–$2,670** | **12.46×** |

At **28 blocks/month on each 20× tier**, the respective API equivalents are **$210, $105, $124.60**; ratios are **1.05×, 0.525×, 0.623×**.

## Other plans and billing

| Plan | Published price | Calculation or data status |
| --- | ---: | --- |
| [ChatGPT Go](OpenAI/goPlan.md) | $8/month | Token allowance unavailable in cited sources; Sol-comparator price equality at 1.07 blocks/month |
| [Google AI Plus](Google/plusPlan.md) | $4.99/month | Assumed 13–15 blocks: $57.85–$66.75 API equivalent |
| [SuperGrok Plus](xAI/superGrokPlan.md) | $100/month | Assumed 26–30 blocks: $104–$120 API equivalent |
| [ChatGPT Business, standard](OpenAI/businessPlan.md) | $25/seat/month; 2-seat minimum | Two seats: $50/month; one active seat at 28 blocks: $210 / $50 = 4.20× |
| [Claude Team, standard / premium](Anthropic/teamPlan.md) | $25 / $125 per seat/month | Standard annual billing: 2 × $20 × 12 = $480 for two seats |
| [Claude Enterprise](Anthropic/teamPlan.md) | $20/seat/month, billed annually, plus API-rate usage | 28 Sonnet blocks: $20 + $105 = $125/seat/month equivalent |

## Published usage conditions

* **OpenAI:** five-hour Codex message estimates; weekly limits may apply. New Pro 20× subscriptions/upgrades have been paused since September 10, with limited return eligibility. [Usage](https://learn.chatgpt.com/docs/pricing), [Pro status](https://help.openai.com/en/articles/9793128-about-chatgpt-pro-plans).
* **Anthropic:** Max 5×/20× refers to per-session usage; five-hour sessions and separate weekly limits apply. [Max limits](https://support.claude.com/en/articles/11049741-what-is-the-max-plan).
* **Google:** compute-based five-hour limits and a weekly cap. [Usage change](https://blog.google/products-and-platforms/products/google-one/google-ai-subscriptions/).
* **xAI:** paid products share a weekly usage pool. [Usage FAQ](https://docs.x.ai/grok/faq).

## Cost sensitivity

Fixed token volume; cached costs include the assumed cache creation/storage charges.

| Comparator | Cached block | Uncached block | Calculated cost reduction |
| --- | ---: | ---: | ---: |
| GPT-5.6 Sol | $7.50 | $18.20 | 58.79% |
| Sonnet 5 | $3.75 | $9.10 | 58.79% |
| Gemini 3.1 Pro Preview | $4.45 | $9.40 | 52.66% |
| Grok 4.6 | $4.00 | $8.50 | 52.94% |

**Reduction = 1 − cached cost / uncached cost.** Output/reasoning accounts for **0.15 / 3.95 = 3.80%** of tokens and **40%** of the cached Sol and Sonnet block costs. [Rates and calculations](methodology.md).

## Data coverage

Included: subscription prices, published usage conditions, API list rates, and calculations under stated workload assumptions.

Unavailable in this repository: measured monthly token allowances, subscriber usage distributions, provider serving costs, training expenditure, infrastructure commitments, and consolidated financial data. Provider margins and investment returns are not calculated.
