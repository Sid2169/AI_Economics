# xAI — SuperGrok and SuperGrok Plus

Source check: **2026-09-20**.

## Facts

* SuperGrok: **$30/month**; SuperGrok Plus: **$100/month**. Grok 4.6 is listed; Plus offers higher usage. [Pricing](https://x.ai/pricing).
* Paid usage draws from a shared weekly pool across products. Its token quantity and the Plus-to-SuperGrok multiplier are not published in the cited documentation. [Usage FAQ](https://docs.x.ai/grok/faq).

## Representative usage

Grok 4.6, standard short-context API rates. [Model pricing](https://docs.x.ai/developers/models/grok-4.6).

| Tokens | API cost |
| --- | ---: |
| 3.00M cache reads × $0.50/M | $1.50 |
| 0.80M fresh input × $2/M | $1.60 |
| 0.15M output/reasoning × $6/M | $0.90 |
| **3.95M total** | **$4.00** |

## Monthly estimate — fixed demand

Assume **26–30 blocks/month** on either plan; no unverified tier multiplier:

**26–30 × $4 = $104–$120/month**, central **$112**.

| Plan | Value / price | Break-even blocks/month |
| --- | ---: | ---: |
| SuperGrok | **3.47–4.00×** | **7.50** |
| SuperGrok Plus | **1.04–1.20×** | **25.00** |

Central INR illustration: **₹10,080**, versus converted prices **₹2,700 / ₹9,000**.

## Key findings

* These are demand scenarios; neither plan's included capacity is established in tokens.
* Plus costs **3.33×** as much. It needs more than **3.33× actual usage** to improve the token-value multiple at an unchanged model mix.
* Lite and Heavy appear in the plan comparison, but their current prices were not exposed in the fetched pricing page; no price or quota is inferred here.
* Image/video/voice usage can reduce the pool available for text/code. [Calculation assumptions](../methodology.md).
