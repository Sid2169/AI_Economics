# Google — AI Ultra

Source check: **2026-09-20**.

## Facts

| Tier | US monthly price | Advertised Gemini usage vs Pro |
| --- | ---: | ---: |
| Ultra 5× | $99.99 | 5× |
| Ultra 20× | $199.99 | 20× |

[Current subscription prices](https://gemini.google/subscriptions/). These supersede the original ~$250 Ultra price; Google announced the new tiers in May 2026. [Announcement](https://blog.google/products-and-platforms/products/google-one/google-ai-subscriptions/).

## Representative usage

Gemini 3.1 Pro Preview: **$4.45/block**, including **$0.45** assumed cache storage. [Workload](proPlan.md); [API rates](https://ai.google.dev/gemini-api/docs/pricing#gemini-3.1-pro-preview).

## Monthly estimate — conditional scaling

Assume Pro can complete **26–30 blocks/month** and actual Ultra monthly throughput scales by the advertised ratio:

| Tier | Assumed blocks/month | API equivalent | Central | Value / price |
| --- | ---: | ---: | ---: | ---: |
| Ultra 5× | 130–150 | **$578.50–$667.50** | $623 | **5.79–6.68×** |
| Ultra 20× | 520–600 | **$2,314–$2,670** | $2,492 | **11.57–13.35×** |

Central INR illustrations: **₹56,070 / ₹2,24,280**, against converted prices **₹8,999 / ₹17,999**.

## Key findings

* Break-even: **22.47 / 44.94 blocks/month** for 5× / 20×.
* At unchanged usage of 28 blocks/month, either tier replaces **$124.60** of API usage: **1.25× / 0.62×** its price.
* These are throughput scenarios, not verified maxima. Deep Think and other modes do not necessarily have a one-to-one API comparator; their value is excluded. [Methodology](../methodology.md).
