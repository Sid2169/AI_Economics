# Anthropic — Claude Max

Source check: **2026-09-20**.

## Facts

| Tier | Monthly price | Session capacity relative to Pro |
| --- | ---: | ---: |
| Max 5× | $100 | 5× |
| Max 20× | $200 | 20× |

Sessions reset every five hours; a separate weekly limit applies. The published multiples describe **per-session capacity**, not a quantified monthly token budget. [Max pricing and limits](https://support.claude.com/en/articles/11049741-what-is-the-max-plan).

## Representative usage

Sonnet 5: **3 × $0.20 + 0.7 × $2 + 0.1 × $2.50 + 0.15 × $10 = $3.75/block**. [API rates](https://platform.claude.com/docs/en/about-claude/pricing).

## Monthly estimate — conditional scaling

Let **k = actual monthly throughput / the assumed Pro baseline**. Then:

**V = (26–30) × k × $3.75 = $97.50k–$112.50k.**

| Scenario | Assumed k | API equivalent | Central | Value / price |
| --- | ---: | ---: | ---: | ---: |
| Max 5×, monthly throughput also 5× | 5 | **$487.50–$562.50** | $525 | **4.88–5.63×** |
| Max 20×, monthly throughput also 20× | 20 | **$1,950–$2,250** | $2,100 | **9.75–11.25×** |

**These k values are assumptions; session marketing does not establish them.** At unchanged usage of 28 blocks/month, both plans replace only **$105** of Sonnet API usage: **1.05× / 0.525×** their prices.

## Key findings

* Break-even: **26.67 / 53.33 blocks/month** for Max 5× / 20×.
* Central scaled INR illustrations: **₹47,250 / ₹1,89,000**, against converted prices **₹9,000 / ₹18,000**.
* Fable models can consume up to **50% of the existing weekly allowance**, not an additional allowance. [Fable limits](https://support.claude.com/en/articles/15424964-claude-fable-models-on-your-plan). Fable 5.1 costs **$16.50 per representative block**, but that rate cannot be multiplied by the Sonnet throughput assumption to infer included value. [Workload methodology](../methodology.md).
