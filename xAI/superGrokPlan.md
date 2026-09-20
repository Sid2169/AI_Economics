# xAI — SuperGrok and SuperGrok Plus

Source check: **2026-09-20**.

## Facts

* SuperGrok: **$30/month**; SuperGrok Plus: **$100/month**. Grok 4.6 is listed; Plus offers higher usage. [Pricing](https://x.ai/pricing).
* Paid usage draws from a shared weekly pool across products. Its token quantity and the Plus-to-SuperGrok multiplier are not published in the cited documentation. [Usage FAQ](https://docs.x.ai/grok/faq).

## Assumed workload

Grok 4.6, standard short-context API rates. [Model pricing](https://docs.x.ai/developers/models/grok-4.6).

| Tokens | API cost |
| --- | ---: |
| 3.00M cache reads × $0.50/M | $1.50 |
| 0.80M fresh input × $2/M | $1.60 |
| 0.15M output/reasoning × $6/M | $0.90 |
| **3.95M total** | **$4.00** |

## Monthly calculation — fixed usage

Calculation input: **26–30 blocks/month** on each plan:

**26–30 × $4 = $104–$120/month**, at 28 blocks **$112**.

| Plan | API equivalent / price | Break-even blocks/month |
| --- | ---: | ---: |
| SuperGrok | **3.47–4.00×** | **7.50** |
| SuperGrok Plus | **1.04–1.20×** | **25.00** |

INR calculation at 28 blocks: **₹10,080**, versus converted prices **₹2,700 / ₹9,000**.

## Additional calculations and limits

* Included monthly token capacities are unavailable in the cited sources.
* Price ratio: **$100 / $30 = 3.33×**. At a fixed API cost/block, equal API-equivalent/subscription ratios require the same **3.33×** block-count ratio.
* Lite and Heavy are listed; prices and token quotas were unavailable in the fetched pricing page.
* Image, video, voice, and text/code draw from the shared weekly pool. [Calculation assumptions](../methodology.md).
