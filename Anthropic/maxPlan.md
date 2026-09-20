# Anthropic — Claude Max

Source check: **2026-09-20**.

## Facts

| Tier | Monthly price | Session capacity relative to Pro |
| --- | ---: | ---: |
| Max 5× | $100 | 5× |
| Max 20× | $200 | 20× |

Sessions reset every five hours; a separate weekly limit applies. The published multiples describe **per-session capacity**, not a quantified monthly token budget. [Max pricing and limits](https://support.claude.com/en/articles/11049741-what-is-the-max-plan).

## Assumed workload

Sonnet 5: **3 × $0.20 + 0.7 × $2 + 0.1 × $2.50 + 0.15 × $10 = $3.75/block**. [API rates](https://platform.claude.com/docs/en/about-claude/pricing).

## Monthly calculation — assumed scaling

Let **k = assumed monthly block-count multiplier**. Then:

**V = (26–30) × k × $3.75 = $97.50k–$112.50k.**

| Scenario | Assumed k | API equivalent | At 28 × k blocks | API equivalent / price |
| --- | ---: | ---: | ---: | ---: |
| Max 5×, monthly throughput also 5× | 5 | **$487.50–$562.50** | $525 | **4.88–5.63×** |
| Max 20×, monthly throughput also 20× | 20 | **$1,950–$2,250** | $2,100 | **9.75–11.25×** |

The cited source provides session multiples; monthly k is unmeasured. At **28 blocks/month**, both plans have **$105** Sonnet API equivalent: **1.05× / 0.525×** their prices.

## Additional calculations and limits

* Break-even: **26.67 / 53.33 blocks/month** for Max 5× / 20×.
* INR calculations at 140 / 560 blocks: **₹47,250 / ₹1,89,000**, against converted prices **₹9,000 / ₹18,000**.
* Fable models can consume up to **50% of the existing weekly allowance**, not an additional allowance. [Fable limits](https://support.claude.com/en/articles/15424964-claude-fable-models-on-your-plan). Fable 5.1 costs **$16.50 per assumed block**. Included monthly Fable token throughput is unmeasured. [Workload methodology](../methodology.md).
