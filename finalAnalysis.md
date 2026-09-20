# AI Economics — Overall Analysis

As of **2026-09-20**. Synthesis of this repository's subscription analyses; USD, before tax.

**Under the assumed workload, heavily used subscriptions can replace several times their price in retail API usage. The economic advantage depends on actual permitted usage, model choice, and caching. These comparisons do not establish lab profitability.**

## 1. Comparable workload

One block: **3.95M tokens**, including 3M cache reads, 0.8M fresh input, and 0.15M output/reasoning. Cache creation/storage included. Assume **28 blocks/month**; this is a demand scenario, not a measured allowance. [Methodology and API sources](methodology.md).

| Subscription / API comparator | Monthly price | API cost/block | API equivalent at 28 blocks | Value / price | Break-even blocks/month |
| --- | ---: | ---: | ---: | ---: | ---: |
| [ChatGPT Plus / GPT-5.6 Sol](OpenAI/plusPlan.md) | $20 | $7.50 | **$210** | **10.50×** | 2.67 |
| [Claude Pro / Sonnet 5](Anthropic/proPlan.md) | $20 | $3.75 | **$105** | **5.25×** | 5.33 |
| [Google AI Pro / Gemini 3.1 Pro Preview](Google/proPlan.md) | $19.99 | $4.45 | **$124.60** | **6.23×** | 4.49 |
| [SuperGrok / Grok 4.6](xAI/superGrokPlan.md) | $30 | $4.00 | **$112** | **3.73×** | 7.50 |

Plus is recalculated using the shared methodology and [$20 US price](https://learn.chatgpt.com/docs/pricing); the original sample retains its broader range and Indian price assumption.

**This is not a ranking of model quality or available capacity.** OpenAI's larger multiple partly reflects its higher API comparator price. Equal token counts do not imply equal tasks completed.

## 2. Higher tiers: capacity must be used

Central scenarios assume **140 blocks/month on 5× tiers** and **560 on 20× tiers**:

| Lab / comparator | 5× tier: price → API equivalent | 20× tier: price → API equivalent |
| --- | ---: | ---: |
| [OpenAI / Sol](OpenAI/proPlan.md) | $100 → **$1,050 (10.50×)** | $200 → **$4,200 (21.00×)** |
| [Anthropic / Sonnet](Anthropic/maxPlan.md) | $100 → **$525 (5.25×)** | $200 → **$2,100 (10.50×)** |
| [Google / Gemini](Google/ultraPlan.md) | $99.99 → **$623 (6.23×)** | $199.99 → **$2,492 (12.46×)** |

Monthly scaling is unverified; Claude explicitly describes per-session multiples. New OpenAI Pro 20× subscriptions/upgrades are paused, subject to limited return eligibility. [Current Pro status](https://help.openai.com/en/articles/9793128-about-chatgpt-pro-plans).

At unchanged **28-block usage**, the ~$200 tiers replace only **$105–$210** of API usage. The apparent volume discount disappears when capacity goes unused.

For an upgrade, compare **extra useful API-equivalent usage with the price increase**. A $100 → $200 upgrade needs more than **$100 of additional replacement value**, before valuing features or avoided interruptions. A nominal 4× capacity increase does not provide that automatically.

Other findings:

* [Google AI Plus](Google/plusPlan.md): **$62.30 / $4.99 = 12.48×** at an assumed 14 blocks/month. [ChatGPT Go](OpenAI/goPlan.md): no defensible monthly allowance estimate.
* [Business](OpenAI/businessPlan.md) and [Team](Anthropic/teamPlan.md): minimum seats and unused seats reduce value; annual discounts require an upfront commitment.
* [SuperGrok Plus](xAI/superGrokPlan.md): **$112 / $100 = 1.12×** at unchanged usage; its capacity multiplier remains unknown.

## 3. What drives the economics

**Usage allocation.** Five-hour windows, weekly caps, and shared pools limit how much serving cost a fixed subscription can incur. Google's compute-based limits and Grok's shared pool make task intensity relevant to consumption. Economic inference: the effective price is **subscription cost / useful work completed**; a quota reduction can raise that price without changing the monthly fee. [Google limits](https://blog.google/products-and-platforms/products/google-one/google-ai-subscriptions/), [Grok limits](https://docs.x.ai/grok/faq).

**Caching and reasoning.** For the four primary comparators above, the assumed caching cuts API cost by **53–59%** versus the same token volume without caching. Output/reasoning is only **3.8% of tokens**, but **40% of the Sol and Sonnet block cost**. Long reasoning traces, retries, and repeated agent steps can therefore dominate spending. [Calculations](methodology.md).

**Segmentation and bundles.** The reviewed plans offer low-price entry, ~$20 general use, ~$100–$200 heavier use, and organizational access. Google also bundles storage and other services; Claude Enterprise charges a seat fee plus API-rate usage. Economic inference: providers can charge for convenience, integration, and administration as well as model consumption. [Google bundles](https://gemini.google/subscriptions/), [Claude pricing](https://claude.com/pricing).

## 4. Provider profitability: what can be inferred

Let **P = net subscription revenue**, **V = retail API-equivalent usage**, and **a = actual serving cost / V**.

**Contribution before other expenses = P − aV.**

Illustration: **P = $20, V = $200**.

| Hypothetical a | Serving cost | Contribution |
| --- | ---: | ---: |
| 5% | $10 | +$10 |
| 10% | $20 | $0 |
| 20% | $40 | −$20 |

These are sensitivities, not estimates of any lab's cost. A **10× API-value multiple** requires serving cost below **10% of API retail value** merely to leave a positive contribution for that user. Training, research, product development, sales, and other expenses still require funding.

Across subscribers, the relevant quantity is **Σ revenue − Σ actual serving cost**. Light users could offset heavy users; the usage distribution and costs needed to quantify that are absent. Neither a loss-making heavy user nor a profitable subscription cohort establishes company-wide profitability or returns on infrastructure investment.

## 5. Broader implications

* **Lower unit prices can coexist with higher total spending.** Illustratively, halving price while tripling consumption increases spending **1.5×**. More agent activity could offset efficiency gains; this is a scenario, not a demand forecast.
* **API-value multiples can fall without subscriptions getting worse.** Halving API prices halves the replacement-value multiple at unchanged subscription price and usage. Conversely, a high API list price can inflate the apparent subscription bargain.
* **The useful comparison is cost per successful task.** Include retries, human review, integration effort, and quota interruptions. A cheaper token can become an expensive result if more work is needed to finish the task.
* **Financial sustainability remains unresolved.** This repository supports workload and pricing comparisons. It lacks measured subscriber utilization, actual serving costs, revenue mix, training expenditure, and infrastructure commitments needed to estimate lab margins or investment returns.
