# GPU Cloud Atlas — Top Neoclouds

> **Research brief for Soup** · Snapshot: 8 November 2026  
> **Pack:** Top neoclouds · **Scope:** public information only  
> **Purpose:** identify practical cloud distribution and integration opportunities for Soup, an open-source LLM fine-tuning engine.

## Executive summary

Soup reduces fine-tuning memory pressure by streaming model layers through available GPU memory. That creates a useful cloud proposition: make a provider’s existing GPU instances easier to use for fine-tuning workloads that otherwise require larger-memory or multi-GPU configurations. This is a product-fit hypothesis, not a claim that Soup has been benchmarked or integrated with any provider below.

**Recommended first target: Nebius.** Its current self-service catalog spans several NVIDIA GPU generations and regions in Europe and the US, and its managed AI software stack creates a plausible route to a reproducible Soup image or guided workload. Start with a small compatibility/benchmark pilot, not an enterprise-wide partnership pitch.

**Close alternatives:** Crusoe for a developer-friendly cloud and visible Slurm/Kubernetes/dstack paths; Lambda for a clear menu from single-GPU experiments to large clusters and well-documented cluster tooling. Together AI is a strong strategic target if Soup can demonstrate measurable GPU utilization or fine-tuning economics at scale.

**Important data rule:** GPU product availability, customer reservations, contracted power, announced deployments, and installed GPUs are different measures. This report labels them separately and does not convert megawatts into GPU counts. Several providers do not publish a current company-wide installed fleet.

## How to read the comparison

- **Available models / scale** describes products or configurations advertised publicly. It is not automatically an installed-fleet count.
- **Announced / contracted** describes a public commitment or deployment plan; it may not yet be online.
- **Locations** name publicly described regions or facilities, not a complete global inventory.
- **Soup fit** is our reasoned proposal based on public product information. It is not an existing partnership or endorsement.
- **Sources** are linked inline and listed by provider at the end. Company materials are useful for products and announcements; their claims should be verified in a pilot.

## Provider comparison

| Provider | Public GPU information | Public footprint / stack signals | Public customer or deployment signals | Best Soup angle |
|---|---|---|---|---|
| [CoreWeave](#1-coreweave) | H100/H200 and Blackwell systems; one Barcelona site disclosed 10,224 H200s. Company reported >850 MW active power and ~3.1 GW contracted power in FY2025; these are power figures, not GPU counts. | US and European footprint; Mission Control, Kubernetes/Slurm integrations, managed storage and observability. | IBM, Mistral AI and Cohere named as early GB200 customers; broad AI/software customer list. | Validated, high-throughput fine-tuning templates for managed Kubernetes/Slurm users. |
| [Nebius](#2-nebius) | Self-service catalog lists B300, B200, H200, H100, RTX PRO 6000 and L40S. A 2025 Israel site rollout announced 4,000 HGX B200 GPUs. Its 30,000-GPU Q1 2025 figure is historical, not a current fleet count. | Europe and US self-service regions; announced deployments in Israel and US. Aether platform, NVIDIA AI Enterprise and NeMo/NIM ecosystem. | Multi-year Microsoft capacity deal; large Meta compute agreement announced for 2027 onward. | Reproducible Soup images and a small Nebius catalog/tutorial pilot across GPU tiers. |
| [Lambda](#3-lambda) | On-demand 1–8 GPUs; 1-Click clusters from 16 to 2,000+; supercluster configurations advertised from 4,000 to 165,000+ GPUs. These are service ranges, not installed fleet totals. | US-based facilities noted for government cloud; Kubernetes and Slurm cluster options, preinstalled software. | Public customer stories include Meshy and Kodiak; a separate large-cluster story leaves the customer unnamed. | A simple single-node-to-cluster Soup path with Slurm/Kubernetes examples. |
| [Crusoe](#4-crusoe) | Catalog lists NVIDIA A100 through Vera Rubin generations and AMD MI300X/MI355X. Publicly described 512-GPU B200 validation is a benchmark deployment, not total fleet. | US, Iceland and Norway presence described publicly; Console, CLI, API, Terraform, SDK, Slurm, Kubernetes and dstack integrations. | Customer references include Fireworks, Roboflow, Windsurf, Ollama and Cartesia. | Publish a Soup-ready dstack/Slurm template and benchmark memory savings on available GPUs. |
| [Together AI](#5-together-ai) | Company says tens of thousands of GPUs deployed; announced a 36,000-GPU GB200 NVL72 cluster and 64-to-10,000+ GPU cluster services. Announced cluster size and service range are not equivalent to deployed fleet. | AI cloud and inference/training stack; public announcements describe >200 MW data-center/power capacity. | Salesforce, Zoom, Zomato, ElevenLabs, Hedra and Cartesia appear in public customer materials. | Demonstrate improved fine-tuning throughput-per-dollar or additional model capacity on existing infrastructure. |
| [Nscale](#6-nscale) | Major public plans include ~200,000 GB300 GPUs for Microsoft and a 100,000-GPU Stargate Norway announcement; these are commitments/plans, not verified current installed counts. | UK/European and US infrastructure projects; managed inference, fine-tuning, OpenAI-compatible API, Kubernetes, Slurm and bare metal. | Microsoft and OpenAI/Aker appear in infrastructure announcements. | Package Soup as a managed fine-tuning workflow that complements Nscale’s managed AI services. |
| [Fluidstack](#7-fluidstack) | Public sources reviewed do not establish a current company-wide installed GPU count. It operates marketplace and dedicated/private-cluster models; Nordic H200 deployments have been announced with partners. | Partner/colocation-heavy model; high-touch cluster operations and customer-specific infrastructure. Anthropic announced a $50B US infrastructure program with sites planned through 2026. | Public references include Meta, Poolside, Black Forest Labs, Character.AI and Mistral AI. | Offer Soup as a workload adapter / validated fine-tuning recipe for dedicated customer clusters. |
| [IREN](#8-iren) | Company announced a planned 150,000-GPU AI Cloud capacity including 50,000 B300 purchases, with deployment phases in H2 2026. Product page lists H100/H200/B200/B300/GB300 NVL72. Treat 150,000 as announced capacity, not verified online fleet. | Canadian and US sites, including Mackenzie, BC and Childress, Texas. AI Cloud includes InfiniBand networking. | Microsoft signed a $9.7B / 200 MW agreement; Perplexity announced an AI Cloud agreement. | Build a low-friction Soup image and benchmark for IREN’s latest GPU offerings. |

---

## Provider profiles

### 1. CoreWeave

**What is public.** CoreWeave’s FY2025 results report more than 850 MW of active power and approximately 3.1 GW of contracted power. Both are power-capacity measures, not counts of GPUs. The company separately described its Barcelona facility as a 15 MW site hosting 10,224 H200 GPUs. CoreWeave announced GB200 systems at scale and named IBM, Mistral AI and Cohere among early customers. Its platform describes Mission Control, cluster health validation, observability, Kubernetes and Slurm-related workflows.

**Soup opportunity.** Offer an open-source reference recipe that provisions a supported GPU instance, runs a representative fine-tune, and reports peak VRAM, throughput and quality checks. A more memory-efficient path could help customers test models on smaller allocations before scaling to a managed cluster. CoreWeave’s mature scale and customer base make it attractive, but likely raise the bar for validation and procurement.

**Suggested first step.** Create a reproducible CoreWeave tutorial and ask for technical feedback through a public developer channel; avoid claiming official support until the recipe is tested and accepted.

### 2. Nebius

**What is public.** Nebius’s current self-service catalog lists B300, B200, H200, H100, RTX PRO 6000 and L40S across Europe and US regions. Its announcement for an Israel deployment describes 4,000 HGX B200 GPUs with Quantum InfiniBand and NVIDIA AI Enterprise / NeMo / NIM software. The often-cited 30,000-GPU global figure was reported for Q1 2025 and should be treated as a dated snapshot. Nebius has announced a multi-year infrastructure agreement with Microsoft and a substantial future compute agreement with Meta, including capacity expected from 2027.

**Soup opportunity.** Make Nebius the first integration target: publish tested instance recipes for one smaller-memory tier and one high-end tier, then measure whether layer streaming expands the set of models users can fine-tune. Nebius’s model diversity could make the result useful to researchers choosing between price, memory and throughput. The proposed partnership is a hypothesis based on catalog fit and software ecosystem.

**Suggested first step.** A 2–3 GPU-family pilot with a public benchmark table and one-click or Terraform setup.

### 3. Lambda

**What is public.** Lambda Cloud advertises on-demand 1–8 GPU instances, 1-Click clusters with 16 to 2,000+ GPUs, and supercluster configurations from 4,000 to 165,000+ GPUs. These describe service configurations, not proof that every configuration is presently available or the size of Lambda’s owned fleet. Its documentation covers H100/H200/GB200 configurations and managed or preinstalled Kubernetes/Slurm workflows. Government materials identify US-based data centers and government customers; public customer stories include Meshy and Kodiak.

**Soup opportunity.** Lambda’s product ladder is well suited to a stepped developer story: start with a single GPU, run a fine-tune, then scale the same configuration to a Slurm or Kubernetes cluster. Soup could lower the memory barrier for experimenting before a user books a larger cluster.

**Suggested first step.** Publish tested launch scripts for one-GPU and multi-node Slurm workflows; compare completion time and total GPU cost rather than VRAM alone.

### 4. Crusoe

**What is public.** Crusoe’s cloud catalog lists NVIDIA A100, H100, H200, B200, B300, GB200/GB300 and Vera Rubin offerings, as well as AMD MI300X and MI355X. A public 512-GPU B200 validation cluster demonstrates a particular deployment, not total inventory. The platform exposes a Console, CLI, API, Terraform and SDK; documentation covers Slurm, Kubernetes and dstack integrations. Public customer references include Fireworks, Roboflow, Windsurf, Ollama and Cartesia. Crusoe describes operations in the US, Iceland and Norway.

**Soup opportunity.** Deliver a Soup template through dstack or Slurm, along with cost/performance measurements on more than one GPU tier. Crusoe’s developer tooling and multiple accelerator generations could help users choose when memory-efficient fine-tuning is preferable to simply renting a larger GPU.

**Suggested first step.** Build and validate a small public example against Crusoe’s documented interface, then propose it as a community recipe.

### 5. Together AI

**What is public.** Together AI describes tens of thousands of GPUs deployed and announced a 36,000-GPU GB200 NVL72 cluster. It also advertises cluster services from 64 to 10,000+ GPUs. These are different measures: company-reported deployed scale, a named announced cluster, and service configuration ranges. Company materials describe more than 200 MW of data-center/power capacity. Its public customer materials name Salesforce, Zoom, Zomato, ElevenLabs, Hedra and Cartesia.

**Soup opportunity.** The strongest pitch is measurable economics: whether streaming enables a customer to fine-tune a larger model on a given GPU budget, or improves utilization when a workload is memory-bound. Together AI’s combined training/inference footprint provides a compelling route to test both developer workflows and production economics.

**Suggested first step.** Run a benchmark proposal on a fixed model, dataset, quality target and GPU budget. Report throughput, peak memory and cost so the result is decision-useful.

### 6. Nscale

**What is public.** Nscale has announced large infrastructure commitments, including roughly 200,000 GB300 GPUs for Microsoft and 100,000 NVIDIA GPUs for the Stargate Norway project with OpenAI and Aker. These are announced plans or commitments and must not be presented as GPUs currently online. Nscale describes sites and capacity plans across Europe and the US, plus managed inference, fine-tuning, an OpenAI-compatible API, managed Kubernetes/Slurm and bare-metal services.

**Soup opportunity.** Soup could complement a managed AI platform by providing an open-source, lower-memory fine-tuning path and reproducible jobs that customers can move between supported GPU types. Nscale’s infrastructure scale makes potential impact large, while the project’s announced capacity is also exposed to delivery and commissioning timelines.

**Suggested first step.** Create a provider-neutral Soup deployment bundle, then map it to Nscale’s documented managed service interfaces once availability is confirmed.

### 7. Fluidstack

**What is public.** Fluidstack combines a GPU-cloud marketplace with dedicated private-cloud deployments and often works with data-center partners. Its ClusterMAX Gold announcement and SemiAnalysis’s ClusterMAX analysis describe a high-touch engineering model. Fluidstack has public customer references including Meta, Poolside, Black Forest Labs, Character.AI and Mistral AI. The company announced a $50B American infrastructure program with Anthropic, describing New York and Texas data centers planned to come online through 2026. Its European work has included H200-powered clusters with Dell, NVIDIA and Borealis. The sources reviewed do not establish a current company-wide installed GPU count; do not infer one from investment or power announcements.

**Soup opportunity.** Rather than sell a generic cloud feature, offer a validated adapter for dedicated customer clusters: configuration, memory-aware model loading, monitoring and reproducible fine-tuning runs. This aligns with Fluidstack’s customer-specific engineering approach. It is a fit hypothesis, not a known integration.

**Suggested first step.** Prepare one portable cluster recipe and a short benchmark showing the maximum model size and throughput at a fixed GPU allocation.

### 8. IREN

**What is public.** IREN’s AI Cloud product page lists H100, H200, B200, B300 and GB300 NVL72 systems, with high-speed InfiniBand networking. The company announced AI Cloud capacity of 150,000 GPUs, including purchases of 50,000 B300 GPUs, with deployment phases in H2 2026 at Mackenzie, British Columbia and Childress, Texas. Treat that number as announced future capacity, not a verified online fleet. IREN announced a $9.7B / 200 MW Microsoft agreement and a separate AI Cloud agreement with Perplexity.

**Soup opportunity.** Soup could offer an easy-to-run fine-tuning image that helps developers test whether memory streaming makes newer or larger models practical at an allocated GPU count. The announced B-series expansion makes broad compatibility valuable, but current stock and regional availability must be confirmed before benchmarking claims.

**Suggested first step.** Start with one confirmed, bookable configuration; record software versions and results, then expand the benchmark matrix as new systems come online.

## Prioritization for Soup

| Rank | Provider | Rationale | First deliverable |
|---:|---|---|---|
| 1 | **Nebius** | Current multi-generation catalog, Europe/US availability, AI software ecosystem; a practical place to test portability and memory-versus-cost trade-offs. | Reproducible 2–3 tier benchmark and deployment recipe. |
| 2 | **Crusoe** | Visible developer interfaces and Slurm/Kubernetes/dstack integrations; good open-source template fit. | Validated dstack/Slurm recipe with performance and memory measurements. |
| 3 | **Lambda** | Clear path from small instances to clusters; useful developer onboarding story. | One-GPU quickstart plus scale-out example. |
| 4 | **Together AI** | Strongest potential strategic scale and public focus on AI workloads; needs rigorous economic proof. | Fixed-budget benchmark with throughput, memory and quality results. |
| 5 | **Fluidstack** | High-touch private-cluster model and frontier-lab references; best approached with a concrete customer workload. | Portable dedicated-cluster adapter and benchmark. |
| 6 | **CoreWeave** | Large platform and prominent customers, but enterprise validation and partnership bar may be higher. | Production-quality reference deployment with observability. |
| 7 | **IREN** | Large announced GPU expansion and useful platform range; availability timing is a key gating factor. | Benchmark on a currently bookable configuration. |
| 8 | **Nscale** | Managed AI capabilities align with Soup, but much of the most visible GPU scale is announced/forward-looking. | Provider-neutral bundle, then verify deployment readiness. |

This ranking estimates **near-term integration practicality for an open-source project**, not provider quality, financial strength or absolute GPU capacity. Re-rank after access, pricing, support and workload tests are confirmed.

## Proposed pilot scorecard

For each provider, use the same model, dataset, fine-tuning recipe and quality check. Record:

1. Exact GPU SKU/count, region, instance/cluster type and date tested.
2. Peak allocated VRAM and system RAM; model, sequence length, batch size and precision.
3. Tokens or training steps per second; end-to-end completion time.
4. Output quality check and any instability, retries or node failures.
5. Published on-demand or committed price used and total cost for the run.
6. Deployment friction: setup time, image requirements, scheduler compatibility and storage/network bottlenecks.

A lower VRAM number alone is not a win if throughput, cost or output quality becomes worse. Do not publish comparative performance claims until each run is reproducible and the scope is clear.

## Limitations and follow-up

- This is desk research from public sources, captured on 8 November 2026. Product catalogs, inventory, locations and deal timelines change.
- Provider statements about capacity are not independent verification of operational availability.
- Exact company-wide installed GPU counts were not publicly established for every provider. Power in MW cannot be converted to GPU count without workload-specific assumptions.
- Customer names indicate public references or announcements, not endorsement of Soup.
- No provider has been contacted and no integration is claimed to exist.
- Before a commercial pitch, verify regional availability, pricing, quotas, data-handling terms and whether an open-source integration is welcome.

## Source register

### ClusterMAX context
- [SemiAnalysis — ClusterMAX 3.0](https://newsletter.semianalysis.com/p/clustermax-30-the-industry-standard)

### CoreWeave
- [FY2025 results: active and contracted power, platform and customer updates](https://investors.coreweave.com/news/news-details/2026/CoreWeave-Reports-Strong-Fourth-Quarter-and-Fiscal-Year-2025-Results/)
- [Barcelona facility: 15 MW and 10,224 H200 GPUs](https://investors.coreweave.com/news/news-details/2025/The-Mayor-of-Barcelona-Jaume-Collboni-Inaugurates-Data-Center-Hosting-CoreWeaves-Leading-AI-Cloud-Platform-in-Partnership-with-MERLIN-Edged/default.aspx)
- [GB200 launch and early customers](https://investors.coreweave.com/news/news-details/2025/CoreWeave-Launches-NVIDIA-GB200-Grace-Blackwell-Systems-at-Scale/default.aspx)
- [CoreWeave platform white paper](https://info.coreweave.com/hubfs/Drive%20AI%20Innovation%20at%20Scale%20White%20Paper-1.pdf)

### Nebius
- [Nebius self-service GPU catalog](https://nebius.com/self-service)
- [Blackwell deployment in Israel](https://nebius.com/newsroom/nebius-brings-nvidia-blackwell-to-israel-with-one-of-the-country-s-first-ai-infrastructure-deployments)
- [Meta infrastructure agreement](https://nebius.com/newsroom/nebius-signs-new-ai-infrastructure-agreement-with-meta)
- [Microsoft infrastructure agreement](https://assets.nebius.com/assets/653bfa58-0f46-487a-964b-4e70f6cca6d8/Nebius%20announces%20multi-billion%20dollar%20agreement%20with%20Microsoft%20for%20AI%20infrastructure.pdf)
- [Q1 2025 shareholder letter](https://assets.nebius.com/assets/2ebc1a9b-61e9-4398-bbdb-e8a24a50efe6/Nebius%20Group_Letter%20to%20shareholders_Q12025.pdf)

### Lambda
- [Lambda Cloud overview](https://lambda.ai/cloud)
- [Private cloud documentation](https://docs.lambda.ai/private-cloud/)
- [Hardware documentation](https://docs.lambda.ai/hardware/)
- [Meshy customer story](https://lambda.ai/hubfs/Customer%20Stories/meshy-case-study.pdf)
- [Lambda government cloud](https://lambda.ai/government)

### Crusoe
- [Crusoe Cloud](https://www.crusoe.ai/cloud)
- [GPU pricing and product catalog](https://www.crusoe.ai/cloud/pricing)
- [dstack integration documentation](https://docs.crusoe.ai/third-party-integrations/dstack/overview/)
- [512-GPU B200 Exemplar Cloud announcement](https://www.crusoe.ai/resources/blog/crusoe-recognized-as-an-nvidia-exemplar-cloud)
- [Customer references](https://www.crusoe.ai/resources/customers)

### Together AI
- [NVIDIA Cloud Partner announcement](https://www.together.ai/blog/nvidia-cloud-partner)
- [NVIDIA Blackwell test-drive / customer references](https://www.together.ai/blog/nvidia-blackwell-test-drive)
- [Enterprise inference expansion with IBM Cloud and NVIDIA](https://www.together.ai/blog/expanding-our-enterprise-inference-capacity-with-ibm-cloud-and-nvidia)
- [Together AI trust and customer resources](https://trust.together.ai/resources)

### Nscale
- [Nscale newsroom and infrastructure announcements](https://www.nscale.com/newsroom)
- [AI infrastructure locations and capacity plans](https://www.nscale.com/ai-infrastructure)
- [Nscale service overview](https://www.nscale.com/service-overview?slide=1)

### Fluidstack
- [Fluidstack ClusterMAX Gold announcement](https://fluidstack.io/news/fluidstack-awarded-clustermax-gold-by-semianalysis)
- [SemiAnalysis ClusterMAX 2.0 analysis of Fluidstack’s operating model](https://newsletter.semianalysis.com/p/clustermax-20-the-industry-standard)
- [Anthropic data-center partnership announcement](https://fluidstack.com/news/fluidstack-selected-by-anthropic-to-deliver-custom-data-centers-in-the-us)
- [Fluidstack Series A announcement](https://fluidstack.io/news/series-a-announcement)
- [Macquarie overview: customer references and GPU financing](https://www.macquarie.com/no/en/insights/accelerating-investment-in-compute-infrastructure-for-fluidstack-a-leading-ai-cloud-platform.html)

### IREN
- [AI Cloud GPU offerings](https://www.iren.com/solutions/gpu-cloud/ai-cloud)
- [150,000-GPU AI Cloud capacity announcement](https://iren.com/resources/news/iren-expands-ai-cloud-capacity-to-150000-gpus)
- [Microsoft $9.7B / 200 MW agreement](https://iren.com/resources/blog/iren-signs97-billion-agreement-with-microsoft-to-deploy-ai-cloud-infrastructure)
- [NVIDIA Exemplar Cloud / GB300 NVL72 status](https://www.iren.com/resources/news/nvidia-exemplar-cloud-nvidia-gb300-nvl72-status)
- [Perplexity AI Cloud agreement](https://www.iren.com/resources/blog/perplexity-and-iren-powering-fast-trustworthy-ai-at-scale)
