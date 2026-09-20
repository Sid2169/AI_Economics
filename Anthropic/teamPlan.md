# Anthropic — Claude Team and Enterprise

Source check: **2026-09-20**.

## Facts

| Plan / seat | Monthly billing | Annual billing, monthly equivalent |
| --- | ---: | ---: |
| Team standard | $25 | $20 |
| Team premium | $125 | $100 |
| Enterprise | — | $20 + usage at API rates |

Team supports **2–150 members**. Standard has more usage than Pro; premium advertises **5× standard**. [Pricing](https://claude.com/pricing).

## Assumed workload

Sonnet 5: **$3.75/block** for the [sample workload with cache creation](../methodology.md). [API rates](https://platform.claude.com/docs/en/about-claude/pricing).

## Monthly calculation

Standard scenario: **26–30 blocks/seat/month**, reference **28**. No numeric Pro-to-standard multiplier is assumed.

| Seat scenario | Blocks/month | API equivalent | API equivalent / monthly price |
| --- | ---: | ---: | ---: |
| Standard | 26–30 | **$97.50–$112.50** | **3.9–4.5×** |
| Premium, assuming 5× monthly throughput | 130–150 | **$487.50–$562.50** | **3.9–4.5×** |

Premium's monthly multiplier is an assumption. At **28 blocks/month**, its API-equivalent ratio is **$105 / $125 = 0.84×**.

Two standard monthly seats cost **$50/month**; two annual seats require **$480/year**. With only one active user, the monthly purchase breaks even at **$50 / $3.75 = 13.33 blocks**.

## Enterprise calculation

For one seat at 28 Sonnet blocks/month:

**$20 seat fee + 28 × $3.75 usage = $125/month equivalent**, versus **$105** direct API cost.

The calculation allocates the seat fee and API usage per seat. Enterprise contract minimums are not included.
