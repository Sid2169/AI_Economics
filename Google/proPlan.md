# Google — AI Pro

Source check: **2026-09-20**.

## Facts

* US price: **$19.99/month**; includes **5 TB storage** and advertises **4× Free Gemini usage**. [Subscriptions](https://gemini.google/subscriptions/).
* Gemini uses compute-based five-hour limits and a weekly cap; old daily prompt counts are not the current calculation basis. [Usage change](https://blog.google/products-and-platforms/products/google-one/google-ai-subscriptions/).

## Assumed workload

Gemini 3.1 Pro Preview API comparator, requests ≤200K input tokens. [API pricing](https://ai.google.dev/gemini-api/docs/pricing#gemini-3.1-pro-preview).

| Tokens / storage | API cost |
| --- | ---: |
| 3.00M cache reads × $0.20/M | $0.60 |
| 0.80M fresh input, including cache creation × $2/M | $1.60 |
| 0.15M output/thinking × $12/M | $1.80 |
| 0.10M cached tokens × 1 hour × $4.50/M/hour | $0.45 |
| **Total per block** | **$4.45** |

## Monthly calculation

Calculation input: **26–30 blocks/month**, from the sample assumption:

**26–30 × $4.45 = $115.70–$133.50**; at 28 blocks **$124.60/month**.

* API-equivalent multiple: **5.79–6.68×** subscription price.
* INR calculation at 28 blocks: **₹11,214**, against converted subscription **₹1,799**.
* Break-even: **$19.99 / $4.45 = 4.49 blocks/month**.

## Additional calculations and limits

Storage cost: **$4.50 × million-token-hours**. Without cache hits, the same token volume costs **$9.40/block**. [Assumptions](../methodology.md).

Scope: Gemini text/code. Bundled benefits and other product allowances are excluded.
