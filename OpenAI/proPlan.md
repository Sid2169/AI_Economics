# OpenAI — ChatGPT Pro

Source check: **2026-09-20**.

## Facts

| Tier | Monthly price | Advertised usage relative to Plus |
| --- | ---: | ---: |
| Pro 5× | $100 | 5× |
| Pro 20× | $200 | 20× |

New Pro 20× subscriptions/upgrades have been paused since September 10; existing subscriptions continue, with limited return eligibility. [Pro tiers](https://help.openai.com/en/articles/9793128-about-chatgpt-pro-plans).

Codex publishes five-hour usage estimates; weekly limits may also apply. No fixed token allowance is established by the published message ranges. [Usage documentation](https://learn.chatgpt.com/docs/pricing).

## Representative usage

GPT-5.6 Sol, [sample workload with cache writes](../methodology.md):

**3 × $0.40 + 0.7 × $4 + 0.1 × $5 + 0.15 × $20 = $7.50/block.** [API rates](https://developers.openai.com/api/docs/models/gpt-5.6-sol).

## Monthly estimate — conditional scaling

Assume the sample's **26–30 blocks/month** on Plus, and **5×/20× actual monthly throughput** on Pro. The latter is an extrapolation, not a published token quota.

| Tier | Blocks/month | API equivalent | Central | Value / price |
| --- | ---: | ---: | ---: | ---: |
| Pro 5× | 130–150 | **$975–$1,125** | $1,050 | **9.75–11.25×** |
| Pro 20× | 520–600 | **$3,900–$4,500** | $4,200 | **19.5–22.5×** |

Central INR illustration at ₹90/$: **₹94,500 / ₹3,78,000**, against converted subscriptions of **₹9,000 / ₹18,000**.

## Key findings

* API break-even: **13.33 / 26.67 blocks/month** for Pro 5× / 20×.
* At the same **28 blocks/month**, either tier replaces **$210** of API usage: **2.10× / 1.05×** its price. An upgrade creates value only if extra capacity or features are used.
* Retaining the original sample's broader **$156–$240** baseline instead gives **$780–$1,200 / $3,120–$4,800** under the same scaling assumption.
