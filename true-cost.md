# True Cost of AI

# Methodology

A token is a useful denominator for LLM economics, but **input, cached-input, and output/reasoning tokens are not economically equivalent** because they require different amounts and patterns of computation. MLPerf measures prompt processing through time to first token and token generation through time per output token. ([MLCommons](https://mlcommons.org/2025/09/small-llm-inference-5-1/?utm_source=chatgpt.com))

The first question should therefore be:

> **What is the fully loaded lifecycle cost of producing and serving one unit of model output?**
> 

Then decompose it into four progressively broader cost measures:

| Measure | What it includes |
| --- | --- |
| **1. Marginal inference cost/token** | Accelerator time, electricity, cooling, networking directly caused by inference |
| **2. Fully loaded inference cost/token** | Above + hardware depreciation, idle capacity/utilization losses, datacenter infrastructure, serving systems and inference operations |
| **3. Lifecycle cost/token** | Above + pretraining, post-training, experiments, failed runs, data, research/engineering, evaluations and model development |
| **4. Full business cost/token** | Above + general corporate overhead, sales, administration, financing where appropriate |

For what we are calling the **true cost of AI**, #3 is probably the central quantity:

![image.png](/image.png)

Expand model-development cost as:

![image.png](/image%201.png)

And inference cost as:

![image.png](/image%202.png)

The important variable is then **lifetime token volume**. A $500 million model serving 10 trillion lifetime tokens contributes:

$$
\frac{\$500{,}000{,}000}{10{,}000{,}000{,}000{,}000\ \text{tokens}}
= \$0.00005/\text{token} = \boxed{\$50/\text{1M tokens}}
$$

If it serves only 1 trillion:

$$
\frac{\$500{,}000{,}000}{1{,}000{,}000{,}000{,}000\ \text{tokens}}
= \$0.0005/\text{token} = \boxed{\$500/\text{1M tokens}}
$$

So training/development cost per token cannot be determined without estimating lifetime utilization.

There is empirical precedent for this decomposition. Epoch's model-development estimates separately account for hardware, energy, experiments and R&D staff; for several historical frontier models, it estimated hardware at 47–67% of development cost, staff at 29–49%, and energy at 2–6%. ([Epoch AI](https://epoch.ai/publications/how-much-does-it-cost-to-train-frontier-ai-models?utm_source=chatgpt.com))

I would research the problem in this order:

1. **Inference physics/economics:** FLOPs/token → accelerator throughput → tokens/GPU-hour → hardware and electricity cost → inference cost/token.
2. **Datacenter economics:** utilization, hardware depreciation, networking, memory, power, cooling and idle capacity.
3. **Model-development economics:** final training run + experiments + post-training + data + engineering/R&D.
4. **Amortization:** estimate lifetime tokens served and allocate development cost across them.
5. **Commercial economics:** compare fully loaded cost/token with API revenue/token, subscription revenue and utilization.

The first concrete calculation I would build is therefore:

$$
\boxed{\text{Fully loaded inference cost per 1M tokens}}
$$

Do that before training amortization. Inference has much more observable empirical data—hardware prices, power, throughput and benchmarks—so it gives you a measurable foundation. Then add progressively less observable layers.

Also keep **input tokens, cached input tokens and output tokens separate throughout the model** rather than collapsing them into one token count. That will produce a substantially more defensible estimate.

# Critical Data points required for these calculations

You need data in five buckets:

| Bucket | Required data |
| --- | --- |
| **1. Model architecture / workload** | Parameter count, active parameters per token, architecture type (dense/MoE), precision, context length, KV-cache requirements, FLOPs per input/output token, average input/output lengths, reasoning-token usage, cache-hit rate |
| **2. Inference infrastructure** | Accelerator type and price, accelerators/server, useful hardware lifetime, measured tokens/s or requests/s, batch size, utilization %, memory requirements, CPU/RAM/storage costs, networking hardware, power consumption, PUE/cooling overhead, electricity price, datacenter/colocation cost |
| **3. Model development** | Number and type of training accelerators, training duration, utilization, training FLOPs, electricity, hardware depreciation/rental, data acquisition/licensing/cleaning, pretraining runs, failed/experimental runs, post-training/RL, evaluations, researcher/engineer compensation and other development infrastructure |
| **4. Operations** | Inference/platform engineering staff, reliability/SRE, monitoring, security, storage, bandwidth, model deployment, moderation/safety systems, customer-support infrastructure, and other recurring serving expenses |
| **5. Amortization / demand** | Lifetime tokens served, tokens served per day/month, model useful lifetime, input/output/cached-token mix, utilization over time, growth/decline in demand, number of replicas/regions and unused reserved capacity |

From these you can calculate three main quantities:

Cost categories must not overlap: for example, use hardware rental or ownership depreciation for the same capacity, without counting both. The lifecycle sum requires a consistent token denominator and inference cost averaged over the model's lifetime; a shorter-period inference average is an estimate of that lifetime average.

$$
{Inference Cost/token} = \frac{\text{total inference-system cost over period}} {\text{tokens served over period}}
$$

$$
Development Cost/token = \frac{\text{total model-development cost}} {\text{lifetime tokens served}}
$$

$$
\boxed{ \text{Lifecycle cost/token} = \text{Inference cost/token} + \text{Development cost/token} }
$$

The hardest data to obtain for closed labs are usually **actual accelerator utilization, model architecture/FLOPs, experimental training expenditure, lifetime token volume, cache rates, and real hardware/datacenter costs**. Those will dominate the uncertainty in an OpenAI-specific estimate.
