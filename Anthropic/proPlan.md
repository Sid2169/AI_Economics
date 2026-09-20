# Anthropic — Claude Pro

Source check: **2026-09-20**.

## Facts

* **$20/month**, or **$200/year = $16.67/month** before tax. [Pricing](https://claude.com/pricing).
* Five-hour sessions and weekly limits apply. Claude Code is included; API billing is separate. [Pro limits](https://support.claude.com/en/articles/8325606-what-is-the-pro-plan).
* Claude and Claude Code share subscription usage. [Shared limits](https://support.claude.com/en/articles/11145838-use-claude-code-with-your-pro-or-max-plan).

## Assumed workload

Sonnet 5 comparator; [API rates](https://platform.claude.com/docs/en/about-claude/pricing):

| Tokens | API cost |
| --- | ---: |
| 3.00M cache reads × $0.20/M | $0.60 |
| 0.70M ordinary input × $2/M | $1.40 |
| 0.10M 5-minute cache writes × $2.50/M | $0.25 |
| 0.15M output/reasoning × $10/M | $1.50 |
| **3.95M total** | **$3.75** |

## Monthly calculation

Calculation input: **26–30 blocks/month**, from the sample assumption:

**26–30 × $3.75 = $97.50–$112.50/month**; at 28 blocks **$105**.

* Monthly subscription multiple: **4.88–5.63×**.
* Annual subscription multiple: **5.85–6.75×**, requiring $200 upfront.
* INR calculation at 28 blocks: **₹9,450** versus converted monthly price **₹1,800**.
* Break-even: **$20 / $3.75 = 5.33 blocks/month**.

## Additional calculations and limits

The same token volume priced with Opus 5 is **$9.375/block**, or **$243.75–$281.25/month**. Monthly token throughput by model is unmeasured. See [methodology](../methodology.md).

Fable 5/5.1 requires extra usage credits on Pro; it is excluded from included-usage estimates. [Fable access](https://support.claude.com/en/articles/15424964-claude-fable-models-on-your-plan).
