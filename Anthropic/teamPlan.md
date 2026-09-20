# Anthropic — Claude Team and Enterprise

Source check: **2026-09-20**.

## Facts

| Plan / seat | Monthly billing | Annual billing, monthly equivalent |
| --- | ---: | ---: |
| Team standard | $25 | $20 |
| Team premium | $125 | $100 |
| Enterprise | — | $20 + usage at API rates |

Team supports **2–150 members**. Standard has more usage than Pro; premium advertises **5× standard**. [Pricing](https://claude.com/pricing).

## Representative usage

Sonnet 5: **$3.75/block** for the [sample workload with cache creation](../methodology.md). [API rates](https://platform.claude.com/docs/en/about-claude/pricing).

## Monthly estimate — conditional

Standard scenario: **26–30 blocks/seat/month**, central **28**. No numeric Pro-to-standard multiplier is assumed.

| Seat scenario | Blocks/month | API equivalent | Value / monthly price |
| --- | ---: | ---: | ---: |
| Standard | 26–30 | **$97.50–$112.50** | **3.9–4.5×** |
| Premium, assuming 5× monthly throughput | 130–150 | **$487.50–$562.50** | **3.9–4.5×** |

Premium's monthly scaling remains an assumption subject to weekly limits and demand. At unchanged 28-block usage, its value is **$105 / $125 = 0.84×**.

Two standard monthly seats cost **$50/month**; two annual seats require **$480/year**. With only one active user, the monthly purchase breaks even at **$50 / $3.75 = 13.33 blocks**.

## Enterprise calculation

For one seat at 28 Sonnet blocks/month:

**$20 seat fee + 28 × $3.75 usage = $125/month equivalent**, versus **$105** direct API cost.

The seat fee is an access/admin charge; it is not an included token budget. Contract terms and organization minimums must be checked separately. This is a per-seat allocation, not a one-seat purchase quote.
