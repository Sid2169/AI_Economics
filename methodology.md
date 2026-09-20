# Methodology

Source check: **2026-09-20**. USD unless stated otherwise.

## Assumed workload

One **block** uses the sample's 3.95M tokens across multiple requests:

| Token category | Millions |
| --- | ---: |
| Cache reads | 3.00 |
| Ordinary input | 0.70 |
| Cache creation input | 0.10 |
| Output, including billed reasoning | 0.15 |
| **Total** | **3.95** |

The sample's 0.80M fresh input is split to account for cache creation. Assume requests stay below each model's long-context pricing threshold; aggregate session tokens are not a single context window. Anthropic uses 5-minute cache writes. Google assumes 0.10M cached tokens stored for one hour per block, with creation input included above.

**C = 3 × read rate + 0.7 × input rate + 0.1 × write rate + 0.15 × output rate + storage.** Rates below are $/1M tokens; storage is $/block.

| API comparator | Input | Read | Write | Output | Storage | C |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| [GPT-5.6 Sol](https://developers.openai.com/api/docs/models/gpt-5.6-sol) | 4 | 0.40 | 5 | 20 | 0 | **7.50** |
| [Claude Sonnet 5](https://platform.claude.com/docs/en/about-claude/pricing) | 2 | 0.20 | 2.50 | 10 | 0 | **3.75** |
| [Claude Opus 5](https://platform.claude.com/docs/en/about-claude/pricing) | 5 | 0.50 | 6.25 | 25 | 0 | **9.375** |
| [Claude Fable 5.1](https://platform.claude.com/docs/en/about-claude/pricing) | 10 | 0.25 | 12.50 | 50 | 0 | **16.50** |
| [Gemini 3.1 Pro Preview](https://ai.google.dev/gemini-api/docs/pricing#gemini-3.1-pro-preview) | 2 | 0.20 | 2 | 12 | 0.45 | **4.45** |
| [Grok 4.6](https://docs.x.ai/developers/models/grok-4.6) | 2 | 0.50 | 2 | 6 | 0 | **4.00** |

Sol pricing is promotional through at least November 21, 2026. Calculations use the listed API comparators; task completion and model quality are unmeasured.

## Monthly calculation

* Sample assumption: **6–7 × 4.33 ≈ 26–30 blocks/month**. **28** is a reference input, not a measured average. The range is not a statistical confidence interval.
* API equivalent: **V = N × C**; price multiple: **V / P**; API/subscription price equality (break-even): **P / C blocks/month**. **P** is subscription price; **N** is monthly blocks.
* For an assumed monthly multiplier **k**, **N = 26k–30k**, reference **28k**. These monthly multipliers are calculation inputs, not measured quotas.
* Block counts measure aggregate token volume across requests; they do not specify elapsed time.
* INR illustration: **USD × 90**, retained from the sample; not verified Indian checkout prices. Comparisons use US prices consistently, before tax.

## Sensitivity

With no cache hits, the same workload is **3.8M ordinary input + 0.15M output**:

| Comparator | Cached block | Uncached block |
| --- | ---: | ---: |
| GPT-5.6 Sol | $7.50 | $18.20 |
| Sonnet 5 | $3.75 | $9.10 |
| Opus 5 | $9.375 | $22.75 |
| Fable 5.1 | $16.50 | $45.50 |
| Gemini 3.1 Pro Preview | $4.45 | $9.40 |
| Grok 4.6 | $4.00 | $8.50 |

Sensitivity calculations hold token volume fixed. Included throughput under different caching/model settings is unmeasured. Google storage cost is **$4.50 × million-token-hours**; this workload assumes **0.10 million-token-hours = $0.45**.

Excluded: tool fees, media, fast-mode premiums, taxes, API discounts, and extra usage purchases. Provider compute costs, profits, and measured subscriber usage are unavailable in this dataset.
