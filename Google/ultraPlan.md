# Google — AI Ultra

Source check: **2026-09-20**.

## Facts

| Tier | US monthly price | Advertised Gemini usage vs Pro |
| --- | ---: | ---: |
| Ultra 5× | $99.99 | 5× |
| Ultra 20× | $199.99 | 20× |

[Current subscription prices](https://gemini.google/subscriptions/). These supersede the original ~$250 Ultra price; Google announced the new tiers in May 2026. [Announcement](https://blog.google/products-and-platforms/products/google-one/google-ai-subscriptions/).

## Assumed workload

Gemini 3.1 Pro Preview: **$4.45/block**, including **$0.45** assumed cache storage. [Workload](proPlan.md); [API rates](https://ai.google.dev/gemini-api/docs/pricing#gemini-3.1-pro-preview).

## Monthly calculation — assumed scaling

Calculation inputs: **26–30 blocks/month × k**, with **k = 5 or 20**. Monthly token allowances are unmeasured:

| Tier | Assumed blocks/month | API equivalent | At 28 × k blocks | API equivalent / price |
| --- | ---: | ---: | ---: | ---: |
| Ultra 5× | 130–150 | **$578.50–$667.50** | $623 | **5.79–6.68×** |
| Ultra 20× | 520–600 | **$2,314–$2,670** | $2,492 | **11.57–13.35×** |

INR calculations at 140 / 560 blocks: **₹56,070 / ₹2,24,280**, against converted prices **₹8,999 / ₹17,999**.

## Additional calculations and limits

* Break-even: **22.47 / 44.94 blocks/month** for 5× / 20×.
* At **28 blocks/month**, either tier has **$124.60** API-equivalent expenditure: **1.25× / 0.62×** its price.
* Monthly block counts are assumed. Deep Think and other modes are excluded. [Methodology](../methodology.md).
