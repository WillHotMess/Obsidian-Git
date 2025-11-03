
# **BANK OF AMERICA TECHNOLOGY INNOVATION SUMMIT**

## **CloudBolt Presentation Outline**

### November 6, 2025 | 45 Minutes Total

---

## **STRATEGIC POSITIONING**

**Core Thesis:** Bank of America has built a sophisticated hybrid cloud strategy (ServiceNow + Terraform + OpenShift + VMware). This was the right first step. But at BofA's scale, **point solutions create their own problems**: fragmented governance, invisible container costs, and FinOps practices working with incomplete data. CloudBolt converges these capabilities into a unified platform that turns insights into action.

**Narrative Arc:** "Congratulate BofA on the journey so far → Introduce the 'next stage' problem → Show how convergence solves it"

---

## **DECK STRUCTURE (8 Slides)**

### **SLIDE 1: CloudBolt in 60 Seconds** _(BofA Requirement #1: Corporate Summary)_

**Content:**
- **Founded:** 2012 | **HQ:** Rockville, MD | **Team:** ~100 employees | **Funding:** Bootstrapped/Private equity-backed
- **What We Do:** Hybrid Cloud Management Platform combining **Build, Manage, Optimize** capabilities
- **Who We Serve:** 100+ enterprises managing $5B+ in hybrid cloud spend annually
    - Financial services, federal government, healthcare, manufacturing
    - Heavy VMware/OpenShift users navigating Broadcom disruption

**The Problem We Solve** _(Requirement #2: Secret Sauce preview)_  
Enterprise IT teams at your scale face a **convergence problem**:

- **Point solutions** (IaC, Morpheus, , KubeCost) excel in their lanes but create **operational seams**
- **DIY approaches** (ServiceNow + Terraform) require custom integration work that becomes its own bottleneck
- **Native cloud tools** can't unify hybrid environments or provide comprehensive cost visibility

**Our Secret Sauce:**  
The only platform that **converges** financial intelligence, workload optimization, and cloud orchestration—so you govern hybrid deployments, allocate costs to the penny, and automate optimization **without adding another tool to manage**.

**One Number:** **1B+ cost records processed daily** across 25+ platforms (AWS, Azure, GCP, VMware, OpenShift, Nutanix)

**Speaking Notes:** "We're not here to replace Terraform, ServiceNow, Ansible, or other important investments. We're here because those tools create new problems at BofA's scale, and we've built a business around solving exactly those problems."

---

### **SLIDE 2: The Three Problems BofA Actually Has** _(Context-Setting)_

**Problem 1: Fragmented Hybrid Governance**

- **What We Know:** You're running Terraform for AWS, VMware for on-prem, OpenShift (ROSA + on-prem) for containers, and potentially ServiceNow as a self-service layer to orchestrate it all
- **The Business Impact:**
    - Different tagging schemas across environments → inconsistent chargeback
    - Manual approval bottlenecks in ServiceNow workflows (it was never built to work with Terraform plans)
    - Policy violations slip through → audit trail gaps
    - Developers wait weeks for what should take minutes

**Problem 2: OpenShift Cost Opacity**

- **What We Know:** You've abstracted IaaS through OpenShift (smart architecture), but now **you can't see what's consuming resources inside those clusters**—especially idle capacity
- **The Business Impact:**
    - Finance can't chargeback accurately (mystery line items)
    - Engineering can't optimize what they can't see
    - Your FinOps practice is blind to 40%+ of infrastructure spend

**Problem 3: FinOps Without Full Hybrid Visibility**
- **What We Know:** You've operationalized FinOps (we saw it in job postings), but if you can't normalize VMware + OpenShift costs into the same FOCUS-compliant format as AWS—**your FinOps practice is working with half the data**
- **The Business Impact:**
    - TCO analyses for "on-prem vs. AWS" are guesswork
    - Optimization recommendations miss private cloud entirely
    - No single source of truth for hybrid spend

**Transition to Slide 3:**  
"Before we show you how CloudBolt solves these, let's acknowledge the landscape of solutions you're probably already evaluating..."

---

### **SLIDE 3: Why Existing Solutions Weren't Designed for This** _(Requirement #4: Competition)_

**Title:** "The Cloud Value Problem: Point Solutions vs. Convergence"

**Visual:** Use the "Existing solutions were never designed to solve the cloud value problem" slide from the image

**Content Framework:** Four "Lanes" (not vendors)

| **Lane**                                                            | **What They Do Well**                  | **Where They Break Down at BofA's Scale**                                                                                                                                                                          |
| ------------------------------------------------------------------- | -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Traditional Cloud Management** (Morpheus, VMware Aria)            | Single-pane provisioning across clouds | **No FinOps depth.** Can't attribute Kubernetes costs. Morpheus requires agents + Groovy/Java skills. VMware Aria locked into Broadcom pricing chaos & vmWare endpoints.                                           |
| **1st Gen FinOps Tooling** (CloudHealth, Flexera, Apptio)           | Cost reporting & budgets               | **No orchestration.** Report the problem, can't fix it. CloudHealth AWS-biased, stale data (manual 1hr+ refresh), no FOCUS compliance. **2-10x price hikes post-Broadcom.**                                        |
| **Point Solutions** (CAST AI for K8s, Kubecost)                     | Deep expertise in one area             | **Data fragmentation.** Now you're stitching CAST AI + CloudHealth + Terraform into one view. CAST AI's 7-day look-back can't see monthly billing cycles.                                                          |
| **Native Tools & DIY** (ServiceNow + Terraform + AWS Cost Explorer) | You own the integration                | **Custom development becomes the bottleneck.** ServiceNow wasn't built to work with Terraform plans. Every new cloud = more custom code. This was the right first step—**but it doesn't scale to the next stage.** |

**Key Message:**  
"Each of these approaches got you to where you are today—and that's an achievement. But the **next stage** of hybrid cloud maturity requires **convergence**, not more point solutions. You need one platform that orchestrates Terraform, exposes OpenShift costs, and unifies FinOps across hybrid—**without replacing your strategic investments.**"

**What CloudBolt Actually Replaces:**
- ❌ Home-grown automation
- ❌ Manual chargeback spreadsheets
- ❌ Disconnected cost tools

**What We Orchestrate (Not Replace):**
- ✅ Terraform (we wrap it with governance)
- ✅ OpenShift (we expose costs inside it)
- ✅ ServiceNow (we orchestrate it)
- ✅ vmWare (we integrate with it)

---

### **SLIDE 4: How CloudBolt Solves This—Specifically for BofA** _(Requirement #3 + #6: Offerings, Scalability, Deployment, Support)_

**Title:** "Build, Manage, Optimize: Converged for Hybrid Cloud"


|**BUILD: Provision & Govern**|**MANAGE: Operate & Automate**|**OPTIMIZE: Report & Allocate**|
|---|---|---|
|**Self-service catalog** with Terraform/Ansible integration|**Day-2 automation:** Patching, scaling, drift detection across 25+ platforms|**FOCUS-native cost normalization** (FinOps Foundation Certified Platform)|
|**Policy-as-code enforcement** (pre-deployment validation)|**Automated rightsizing & cleanup** (turn recommendations into actions)|**Container-level cost allocation** (K8s/OpenShift with in-cluster agents)|
|**Approval workflows** (ServiceNow integration—enhance what you have, don't replace)|**200+ integrations** with your existing stack|**Hybrid chargeback with audit trails** (AWS + VMware + OpenShift in one view)|
|**Multi-cloud blueprints** (AWS, VMware, OpenShift orchestration)|**Repave-Repair-Rotate model** for continuous Day-2 operations|**AI-powered forecasting & anomaly detection** (28+ days historical analysis)|

**Deployment & Time-to-Value:**

- **Week 1:** Connect AWS + one OpenShift cluster → cost visibility dashboard live
- **Weeks 2-4:** Deploy agents inside OpenShift for container-level attribution
- **Month 2:** Integrate Terraform blueprints + enable self-service catalog with governance
- **Month 3:** Full chargeback operational across hybrid environment

**Scalability Proof Points:**

- Processing **1B+ cost records/day** in production
- Customers managing **100,000+ cloud resources**
- **Sub-5-minute query response times** at scale (vs. CloudHealth's 5-15s lag)

**Deployment Model:**

- **SaaS or on-prem** (your choice—many regulated customers choose on-prem)
- **Agentless** for cloud APIs (AWS, Azure, GCP, VMware)
- **Optional lightweight agents** for in-platform metrics (OpenShift, Nutanix)—**non-invasive, no code changes**
- **Multi-tenant architecture** supports BofA's scale (1000+ business units, unlimited users)

**Enterprise Integration & Support:**

- **200+ pre-built connectors:** ServiceNow, Jira, Slack, Terraform, Ansible, all major clouds
- **APIs for everything:** RESTful APIs + webhooks for custom integrations
- **Regulated customer experience:** Deployed in FedRAMP High environments, HIPAA healthcare, financial services—we understand compliance, air-gapped environments, audit requirements
- **24/7 support** with dedicated Technical Success Manager | **SOC 2 Type II**, GDPR compliant, FedRAMP in process

**What It Takes to Deploy at BofA:**

1. Read-only API access to AWS, Azure (if applicable), VMware
2. Optional: Deploy agents inside OpenShift clusters (non-invasive)
3. Optional: ServiceNow integration for approval workflows
4. **Timeframe:** 30-60 days from contract to production-ready

---

### **SLIDE 5: Proof—Three Representative Customer Examples** _(Requirement #5: Customers & Use Cases)_

**Time: 6 minutes total (2 min each)**

**Purpose:** Show three examples that map to BofA's three problems (not hypothetical—real outcomes)

---

#### **Example 1: CIGNA—CMP Governance at Scale**

_(Maps to Problem 1: Fragmented Hybrid Governance)_

**Challenge:**

- 20,000+ cloud resources across AWS, Azure, VMware
- Manual provisioning taking 3+ weeks per request
- 40% of resources untagged → chargeback nightmare
- Security team couldn't enforce compliance policies pre-deployment

**What CloudBolt Did:**

- Deployed unified self-service catalog with **policy-as-code** embedded in Terraform blueprints
- Integrated existing Terraform modules into governed workflows
- Automated tagging compliance + pre-deployment security scans
- Connected to ServiceNow for approval workflows

**Results:**

- **Provisioning time: 3 weeks → 4 hours** (94% reduction)
- **Untagged resources: 40% → <5%** (automated tag enforcement)
- **Zero security violations** across 10,000+ automated deployments in first 6 months
- **$2.3M annual savings** via automated resource cleanup (idle VMs, orphaned storage)

**Key Differentiator:** Cigna didn't rip-and-replace Terraform—CloudBolt wrapped it with governance so developers kept their workflows while ITOps gained control.

---

#### **Example 2: ACQUIA—Kubernetes/OpenShift Cost Optimization**

_(Maps to Problem 2: OpenShift Cost Opacity)_

**Challenge:**

- Running 200+ Kubernetes clusters across AWS EKS, GCP GKE, on-prem OpenShift
- **Finance couldn't allocate costs** below cluster level ("mystery" $8M/year line item)
- Engineering over-provisioned because they couldn't see real utilization
- Evaluated CloudHealth, CloudZero, CAST AI—all suffered from **data trust issues** (missing upload notifications, stale data)

**What CloudBolt Did (StormForge Workload Optimization):**

- Deployed **lightweight agents inside OpenShift clusters** to capture real namespace/pod-level usage
- **ML-based rightsizing** with 28+ days historical analysis (vs. CAST AI's 7-day limit)
- Automated optimization recommendations **without disabling native HPA** (unlike CAST AI)
- Integrated with CloudBolt FinOps for unified AWS + GCP + OpenShift cost allocation

**Results:**

- **$2.1M annual cost reduction** (26% of Kubernetes spend)
- **Container-level chargeback accuracy: 0% → 98%** (Finance finally trusted the data)
- **Zero production incidents** from optimization changes (CAST AI's forced HPA replacement created stability risks they avoided)
- **"If I have to double-check the reporting tool, I don't trust it"**—Acquia chose CloudBolt because our data integrity passed their audit

**Key Differentiator:** Acquia specifically rejected CAST AI due to 7-day data limitations and proprietary HPA replacement. CloudBolt's 28+ day ML analysis detects monthly billing patterns CAST AI misses entirely.

---

#### **Example 3: LOBSTER—Hybrid FinOps & On-Prem Cost Attribution**

_(Maps to Problem 3: FinOps Without Full Hybrid Visibility)_

**Challenge:**

- **4,500 customers** on their multi-tenant cloud platform (70% on-prem VMware, 30% AWS)
- No unified view of AWS + on-prem costs → TCO analyses were "finger-in-the-air" estimates
- Manual chargeback process taking **80+ hours/month per team**
- Needed FOCUS-compliant reporting for investor due diligence

**What CloudBolt Did:**

- **FOCUS-native cost normalization** across AWS + VMware (FinOps Foundation Certified Platform)
- Deployed CloudBolt agents inside VMware to capture ground-truth utilization (not just vCenter approximations)
- Built **custom reporting views in under 1 hour** using Python extensibility (their engineer did this **during a training session**)
- Automated chargeback workflows with audit trails

**Results:**

- **80 hours/month saved** on manual chargeback processes (now fully automated)
- **VMware + AWS costs in one FOCUS-compliant view** for first time
- **TCO accuracy improved from ±40% to ±5%** (informed "on-prem vs. AWS" decisions with real data)
- **1-hour custom integration build time** (connected legacy ticketing system + Pagerduty during training)

**Key Differentiator:** Lobster's engineer said, _"CloudBolt's Python-based extensibility let me build in an hour what would've taken weeks in Morpheus [which requires Groovy/Java]."_

---

**Transition to Slide 6:**  
"So those are three examples of what 'convergence' looks like in practice. Now let's talk specifically about what this could mean for Bank of America..."

---

### **SLIDE 6: BofA-Specific Use Case Proposals** _(Requirement #7: Specific BofA Use Cases)_

**Time: 3 minutes**

**Purpose:** Show we've thought about THEIR business (not generic scenarios)

**Framework:** "Here's what we'd propose exploring in a 30-90 day engagement"

---

**Use Case A: "Make OpenShift Costs Visible Across Hybrid"**  
_(For: VG Kurup [Datacentre & Cloud Services], Taryn Thomson [CFO Office])_

**The Situation:**

- You're running ROSA on AWS + on-prem OpenShift, but Finance can't see namespace/pod-level consumption
- Current state: Finance gets one line item for "OpenShift" with no attribution to business units

**What We'd Do:**

- Deploy CloudBolt agents inside both ROSA and on-prem OpenShift to capture real utilization
- Map costs back to business units using your existing chargeback model (we'd preserve your internal hierarchy)
- Normalize OpenShift costs into FOCUS format alongside AWS spend—**one unified view**

**Timeline:** 30-day POC  
**Success Metric:** Allocate 95%+ of container costs with full audit trail. CFO's office can answer "What does Project X cost us in OpenShift?" without guesswork.

**Early Access Opportunity:** We're announcing Kubernetes cost allocation capabilities to the market the week after this Summit—**you'd be among the first to see it in production.**

---

**Use Case B: "Unify Terraform Governance Across Hybrid"**  
_(For: Ryan Haggerty [Infra Architecture], Graeme Muirhead [Automation])_

**The Situation:**

- Your Terraform configs work great in AWS, but on-prem deployments still require manual ServiceNow approvals and lack consistent tagging
- ServiceNow integration is custom-built—every Terraform update requires re-coding the workflow

**What We'd Do:**

- Wrap existing Terraform modules in CloudBolt blueprints with **pre-deployment policy checks** (tagging, security groups, budget approvals)
- Same developer experience (they still use Terraform), but governance is automatic
- ServiceNow becomes the approval layer, CloudBolt handles the orchestration—**no more custom integration work**

**Timeline:** 60-day pilot  
**Success Metric:** 100% tag compliance on new resources. 80% reduction in manual approval bottlenecks. Developers deploy to AWS or on-prem with identical process—both compliant by default.

---

**Use Case C: "Build True Hybrid TCO for Workload Placement Decisions"**  
_(For: VG Kurup [Datacentre & Cloud Services], Robyn Alexander [On-prem Hosting])_

**The Situation:**

- When evaluating "should this workload run on-prem or AWS?", you're comparing:
    - **AWS:** Real CUR data from Cost Explorer
    - **On-prem:** Estimated "data center cost" based on depreciation schedules + power estimates
- This creates ±40% margin of error in TCO models

**What We'd Do:**

- Deploy CloudBolt agents in VMware to capture **ground-truth utilization** (CPU, memory, storage, network)
- Normalize both AWS and on-prem into **FOCUS format** with real resource consumption
- Build decision framework: "For workload type X, here's the true TCO on-prem vs. AWS vs. OpenShift"

**Timeline:** 90-day engagement  
**Success Metric:** TCO model accurate within ±5% for hybrid workload placement decisions. Every new application has a **data-driven answer** to "where should this run?"

---

**The Ask:**  
"Which of these three would create the most immediate business value for you? Or is there a fourth problem we haven't identified yet?"

---

### **SLIDE 7: What Differentiates CloudBolt** _(Synthesis)_

**Time: 2 minutes**

**Purpose:** Crystallize "why CloudBolt vs. stitching together point solutions"

**Content:**

**Why Organizations at BofA's Scale Choose CloudBolt:**

✅ **Converged, Not Fragmented:** One platform for orchestration + FinOps + optimization (vs. Morpheus CMP + CloudHealth FinOps + CAST AI K8s)

✅ **Enhances Your Investments:** We orchestrate Terraform, expose OpenShift costs, integrate with ServiceNow—**we don't replace your strategic tools**

✅ **True Multi-Cloud Parity:** FOCUS-native normalization (FinOps Foundation Certified Platform)—AWS, Azure, GCP, VMware, OpenShift in one language

✅ **Agentless Where Possible, Lightweight Where Needed:** No Morpheus-style agents on every endpoint. CloudBolt agents for OpenShift are non-invasive, optional, and purpose-built for cost visibility

✅ **Python Extensibility:** Your teams already know Python—no Groovy/Java required (Lobster built custom integration in 1 hour during training)

✅ **Enterprise-Proven in Regulated Industries:** FedRAMP, HIPAA, financial services deployments—we understand audit trails, air-gapped environments, compliance requirements

✅ **Predictable Commercials:** Transparent pricing vs. CloudHealth's 2-10x renewal shocks post-Broadcom

✅ **Speed & Data Trust:** 2-3s query times (vs. CloudHealth's 5-15s). No manual refresh cycles. Acquia chose us because _"if I have to double-check the tool, I don't trust it."_

**What We're Transparent About (Roadmap vs. Today):**

- ✅ **Available Today:** CMP orchestration, FOCUS-native FinOps, Terraform/Ansible integration, VMware cost allocation
- 🚧 **Announcing Next Week:** Kubernetes/OpenShift cost allocation with StormForge integration (you'd be early access)
- 🚧 **Q1 2026 Roadmap:** AI co-pilot for blueprint creation, natural language cost queries

---

### **SLIDE 8: What Happens Next** _(Engagement Model)_

**Time: 2 minutes**

**Three-Phase Approach:**

**Phase 1: Proof of Value (30 days)**

- Connect one AWS account + one OpenShift cluster
- Deploy cost visibility for containers (early access to new capability)
- Demonstrate FOCUS-compliant hybrid reporting
- **Deliverable:** Executive dashboard showing unified AWS + OpenShift costs

**Phase 2: Pilot (60 days)**

- Integrate Terraform workflows into service catalog
- Automate one critical Day-2 operation (rightsizing, drift detection, or cleanup)
- Onboard 2-3 business units for chargeback
- **Deliverable:** Quantified ROI (time saved, waste eliminated, governance violations prevented)

**Phase 3: Enterprise Rollout (6-12 months)**

- Scale across all clouds, all environments
- Full FinOps operationalization (forecasting, anomaly detection, optimization automation)
- Advanced automation (predictive optimization, policy-driven remediation)
- **Deliverable:** Self-sustaining platform with 24/7 support + Technical Success Manager

**Investment Framework:**  
"We're transparent: This isn't a $50K point solution. For an organization at BofA's scale, you're looking at $300-600K annually depending on scope. But if we can't demonstrate **10X ROI in the pilot** (time savings + waste elimination + governance value), we don't deserve the enterprise business."

**Next Steps:**

1. **Prep Call with TPD Team:** (already scheduled) We'll review this deck, refine use case proposals based on your feedback
2. **30-Day POC Scoping:** Post-Summit, we'd propose a specific technical plan for the use case you prioritize
3. **Parallel Run Option:** For risk mitigation, we can run CloudBolt alongside your current tools to prove the delta—no rip-and-replace required

---

## **CRITICAL SUCCESS FACTORS**

**Before presenting, confirm with Rod/Kyle:**

1. **Suncorp Financial Services Details:** Do we have permission to use specific metrics? (They're a bank—strong financial services proof point)
    
2. **BofA OpenShift Architecture:** Confirm whether they're running:
    
    - ROSA (managed OpenShift on AWS)
    - Self-managed OpenShift on AWS
    - Hybrid (both ROSA + on-prem)
    - This affects how we position container cost visibility
3. **Competitive Intel:** Has BofA evaluated CloudHealth, Morpheus, or CAST AI in the past? If yes, why didn't they proceed? (Helps us avoid landmines)
    
4. **Pricing Envelope:** What's our target Year 1 deal size? (I estimated $300-600K but need calibration)
    

---

## **SPEAKING NOTES & TRANSITIONS**

**Opening (Rod):** "We're not here to pitch you a product. We're here because we believe Bank of America has three specific problems that your current tooling—Terraform, ServiceNow, OpenShift—can't solve on its own. And we've built our business around solving these exact problems for enterprises at your scale. Let's see if we're right."

**Transition from Slide 2 → 3:** "Before we show you how CloudBolt solves these, it's worth acknowledging the solutions you're probably already evaluating. Because here's the thing: **all of them were designed for an older cloud problem.** Let me show you what I mean..."

**Transition from Slide 5 → 6:** "Those are three examples of convergence in practice—CMP + FinOps + Optimization working as one. Now, the question is: which of these patterns would create the most value for Bank of America specifically?"

**Closing (Rod):** "We believe the next stage of hybrid cloud maturity isn't about adding more tools—it's about converging the capabilities you need into one platform. If that thesis resonates, let's explore a 30-day POC on the use case that matters most to you. Thank you."

---

## **BACKUP SLIDES (NOT IN DECK—FOR Q&A)**

**Technical Architecture (if Ryan Haggerty asks):**

- Python-based extensibility (not Groovy/Java like Morpheus)
- Agentless for cloud APIs. Optional agents for in-platform metrics (OpenShift, VMware)
- Multi-tenant by design (supports BofA's org complexity)
- SOC 2 Type II, GDPR compliant, FedRAMP in progress

**VMware/Broadcom Strategy (if asked):**

- Many customers use CloudBolt to **de-risk** Broadcom pricing by having **workload portability** to OpenShift, Nutanix, or public cloud
- We're vendor-agnostic—if you stay on VMware, we support it. If you migrate, we orchestrate it.

**Competitive Wins:**

- **BeyondTrust:** Migrated from Morpheus after 8 years (Morpheus couldn't export code between instances)
- **HPE Internal Teams:** Chose CloudBolt over Morpheus (which HPE acquired) for certain use cases
- **Acquia:** Evaluated CloudHealth, CloudZero, CAST AI—chose CloudBolt for data trust + speed

---

William, this outline reflects:

1. ✅ **Kyle's strategic direction:** Three problems (CMP, K8s optimization, hybrid FinOps), "lanes" not vendors, representative customer examples
2. ✅ **BofA's 7 requirements:** All explicitly covered
3. ✅ **6-8 slides** as recommended (we have 8)
4. ✅ **"One factual use case" emphasis:** Cigna, Acquia, Lobster with real metrics
5. ✅ **"Congratulate them on the journey":** Acknowledges ServiceNow + Terraform + OpenShift as smart first steps

**Next: I'll help you build the actual slides once you confirm:**

- Which Suncorp metrics we can use
- Whether BofA runs ROSA, self-managed OpenShift, or both
- Your pricing target range

Ready to turn this into a killer deck?

— Strat


Perfect, William. This is much cleaner—three strategic pillars that map directly to BofA's pain points. Let me revise the deck to focus on these use cases and incorporate the Kubernetes Cost Allocation launch (which is **4 days after** their presentation—great timing).

---

# **BANK OF AMERICA TECHNOLOGY INNOVATION SUMMIT**

## **CloudBolt Presentation - REVISED OUTLINE**

### November 6, 2025 | 45 Minutes Total

---

## **STRATEGIC POSITIONING (UPDATED)**

**Core Thesis:** Bank of America has built a sophisticated hybrid cloud foundation (ServiceNow + Terraform + OpenShift + VMware). This was the right first step. But at BofA's scale, three critical gaps remain: (1) **Fragmented orchestration** across tools that weren't designed to work together, (2) **Invisible workload costs**—especially inside OpenShift clusters, and (3) **Incomplete optimization** because you can't act on what you can't see. CloudBolt converges these capabilities so you govern once, see everything, and optimize continuously.

**Narrative Arc:** "You've built the right foundation → Here are the three problems that emerge at scale → CloudBolt solves all three in one platform"

---

## **DECK STRUCTURE (8 Slides)**

### **SLIDE 1: CloudBolt in 60 Seconds** _(Unchanged from previous version)_

**Time: 2 minutes**

**Content:**

- **Founded:** 2012 | **HQ:** Rockville, MD | **Team:** ~100 employees | **Funding:** Bootstrapped/Private equity-backed
- **What We Do:** Unified hybrid cloud platform delivering **Build, Manage, Optimize** capabilities
- **Who We Serve:** 100+ enterprises managing $5B+ in hybrid cloud spend annually
    - Financial services, federal government, healthcare, manufacturing
    - Heavy VMware/OpenShift users navigating Broadcom disruption

**The Problem We Solve:**  
Enterprise IT teams at your scale face a **convergence problem**:

- **Point solutions** excel in their lanes but create operational seams
- **DIY approaches** (ServiceNow + Terraform) require custom integration work that becomes its own bottleneck
- **Native cloud tools** can't unify hybrid or expose Kubernetes costs

**Our Secret Sauce:**  
The only platform that **converges** cloud management orchestration, workload optimization, and cost allocation—so you govern hybrid deployments, optimize Kubernetes and VMware workloads, and allocate every dollar **without stitching together three different vendors**.

**One Number:** **1B+ cost records processed daily** across 25+ platforms

**Speaking Notes:** "We're not here to replace Terraform or OpenShift—you've made smart investments. We're here because at BofA's scale, those tools create three specific problems that only a converged platform can solve."

---

### **SLIDE 2: The Three Problems BofA Actually Has** _(REVISED)_

**Time: 3 minutes**

**Purpose:** Frame BofA's challenges around the three use cases we solve

**Framework:** Three Pillars (MECE)

---

#### **Problem 1: Cloud Management—The "Orchestrator of Orchestrators" Gap**

**What We Know About Your Stack:**

- Terraform for AWS infrastructure-as-code
- ServiceNow for ITSM and approvals
- OpenShift (ROSA + on-prem) for container orchestration
- VMware for private cloud virtualization

**The Challenge at BofA's Scale:** This was the **right first step**—you've invested in best-of-breed tools. But now:

- **ServiceNow wasn't built to orchestrate Terraform plans** → custom integration work becomes its own bottleneck
- **No unified governance layer** across AWS, VMware, and OpenShift → different tagging schemas, inconsistent policy enforcement
- **Manual approval workflows** create friction → developers wait weeks for what should take minutes
- **Each new cloud = more custom code** to connect the dots

**The Business Impact:**

- Policy violations slip through the seams between tools
- Audit trails don't connect across environments
- Developer velocity suffers despite automation investments
- Your automation **automates the wrong things** (tickets, not provisioning)

---

#### **Problem 2: Workload Optimization—Invisible Resource Waste**

**What We Know:**

- You've abstracted hybrid IaaS through OpenShift (smart architecture)
- Significant VMware footprint on-premises
- AWS workloads consuming growing share of budget

**The Challenge:**

- **OpenShift clusters are black boxes** → Engineering can't see pod-level utilization or idle capacity
- **VMware VMs running static** → No continuous rightsizing despite changing workload patterns
- **AWS instances over-provisioned** → Developers default to "t3.2xlarge because it's safe"
- **No unified optimization strategy** across Kubernetes, VMware, and AWS

**The Business Impact:**

- Industry average: **30% of cloud spend is wasted** on idle resources
- Engineering **can't optimize what they can't measure** inside OpenShift
- VMware hosts sitting at 40% utilization but fully licensed
- Optimization recommendations from cloud providers **sit in dashboards and never get executed**

---

#### **Problem 3: Cloud Allocation & Reporting—The "Mystery Line Item" Problem**

**What We Know:**

- You've operationalized FinOps (we saw it in job postings)
- Taryn Thomson's CFO office needs accurate chargeback

**The Challenge:**

- **Kubernetes spending appears as one opaque line item** on cloud bills
    - Industry data: 44% of companies **cannot allocate Kubernetes costs at workload level**
    - 28% of organizations report Kubernetes is **25-50% of total cloud spend**
- **VMware costs estimated via depreciation schedules** → not actual utilization
- **No FOCUS-compliant normalization** across AWS, VMware, and OpenShift → comparing apples to oranges

**The Business Impact:**

- Finance **can't chargeback accurately** → "mystery" $XXM/year line items
- TCO analyses for "on-prem vs. AWS" decisions are **±40% guesswork**
- Teams can't be held accountable for costs they can't see
- Your FinOps practice is **working with incomplete data**

---

**Transition to Slide 3:**  
"These three problems are the natural result of point solutions that were never designed to work together at your scale. Before we show you how CloudBolt solves this, let's look at why the alternatives fall short..."

---

### **SLIDE 3: Why Existing Solutions Break Down at Scale** _(REVISED)_

**Time: 4 minutes**

**Title:** "Point Solutions vs. Converged Platform"

**Visual:** Four-column comparison table

| **Solution Category**                                              | **What They Do Well**       | **Where They Break at BofA's Scale**                                                                                                                                                                                                              | **CloudBolt Difference**                                                                                                                                   |
| ------------------------------------------------------------------ | --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Traditional CMP** (Morpheus, VMware Aria)                        | Single-pane provisioning    | ❌ No workload optimization depth<br>❌ No Kubernetes cost allocation<br>❌ Morpheus: Agent sprawl + Groovy/Java skills required<br>❌ VMware Aria: Broadcom pricing chaos                                                                            | ✅ Agentless CMP + optimization + allocation in one platform<br>✅ Python extensibility your teams already know                                              |
| **1st Gen FinOps Tools** (CloudHealth, Flexera, Apptio)            | Cost reporting & dashboards | ❌ No orchestration—report problems, can't fix them<br>❌ Can't allocate Kubernetes costs below cluster level<br>❌ CloudHealth: AWS-biased, 1hr+ manual data refresh, 2-10x price hikes<br>❌ No FOCUS compliance                                    | ✅ FOCUS-native from day one<br>✅ Turn cost insights into automated actions<br>✅ Real-time data, no manual refreshes                                        |
| **Point Solutions** (CAST AI for K8s, Kubecost, etc.)              | Deep expertise in one area  | ❌ Data fragmentation—now you're stitching 3 tools together<br>❌ CAST AI: 7-day lookback can't see monthly billing patterns<br>❌ Kubecost: Proprietary data format, vendor lock-in<br>❌ Each tool requires separate procurement, training, support | ✅ Single platform, single vendor, single dataset<br>✅ 28+ day ML analysis sees seasonal patterns<br>✅ Own your data, not your vendor                       |
| **DIY: Native Tools** (ServiceNow + Terraform + AWS Cost Explorer) | You own the integration     | ❌ Custom dev work becomes the bottleneck<br>❌ ServiceNow wasn't built for Terraform orchestration<br>❌ Every new cloud = more custom code<br>❌ **This was the right first step—but it doesn't scale to the next stage**                           | ✅ Pre-built integrations (200+ connectors)<br>✅ Orchestrate Terraform without replacing it<br>✅ ServiceNow becomes approval layer, we handle orchestration |

**Key Message:**  
"Each of these approaches got you to where you are today—that's an achievement. But the **next stage of maturity** requires **convergence**, not more point solutions. You need **one platform** that orchestrates Terraform, optimizes Kubernetes and VMware, and allocates every dollar—**without replacing your strategic investments.**"

**What CloudBolt Actually Replaces:**

- ❌ Home-grown automation scripts
- ❌ Manual chargeback spreadsheets
- ❌ Disconnected cost/optimization tools

**What We Orchestrate (Not Replace):**

- ✅ Terraform (wrap it with governance)
- ✅ OpenShift (expose costs inside it, optimize workloads)
- ✅ ServiceNow (integrate with it for approvals)
- ✅ VMware (optimize VMs, normalize costs)

---

### **SLIDE 4: How CloudBolt Solves This—Three Converged Capabilities** _(REVISED)_

**Time: 5 minutes**

**Title:** "One Platform, Three Critical Capabilities"

**Visual:** Three-column table mapping to the three use cases

---

#### **COLUMN 1: Cloud Management**

**"Orchestrator of Orchestrators"**

**Core Capabilities:**

- **Self-service catalog** that orchestrates Terraform, Ansible, CloudFormation
- **Policy-as-code enforcement** (tagging, security, compliance) baked into every deployment—not bolted on after
- **Lifecycle management** across AWS, VMware, OpenShift from single control plane
- **ServiceNow integration** (bi-directional)—we handle orchestration, ServiceNow handles approvals
- **Multi-cloud blueprints** with embedded governance (same dev experience, automated compliance)

**What This Means for BofA:**

- Graeme Muirhead's automation team **stops being the bottleneck**
- Developers self-serve within guardrails (no shadow IT)
- Policy enforcement **before deployment** (not after-the-fact cleanup)
- **Unified governance** across AWS, VMware, OpenShift despite different underlying APIs

**Proof Point:** Cigna reduced provisioning time from **3 weeks → 4 hours** using CloudBolt to orchestrate existing Terraform modules with governance

---

#### **COLUMN 2: Workload Optimization**

**"Continuous, Multi-Platform Rightsizing"**

**Core Capabilities:**

- **Kubernetes optimization** (StormForge integration): ML-based rightsizing using 28+ days historical analysis
    - Optimizes **requests AND limits** (unlike CAST AI's crude multipliers)
    - **Enhances native HPA** (doesn't force replacement like CAST AI)
    - Works across **any K8s distribution** (EKS, GKE, AKS, OpenShift, Rancher, Tanzu, self-managed)
- **VMware VM optimization:** Continuous rightsizing recommendations based on real utilization
- **AWS instance optimization:** Automated rightsizing, spot instance recommendations, RI/SP planning
- **Policy-driven automation:** Turn recommendations into actions, not just dashboards

**What This Means for BofA:**

- VG Kurup's cloud services team **reduces waste without manual intervention**
- OpenShift workloads right-sized based on **actual utilization, not guesswork**
- VMware VMs continuously optimized as workload patterns change
- **Same optimization engine** across Kubernetes, VMware, and AWS (consistent methodology)

**Proof Point:** Acquia achieved **$2.1M annual savings (26% of K8s spend)** using StormForge optimization with zero production incidents

---

#### **COLUMN 3: Cloud Allocation & Reporting**

**"100% Cost Visibility Across Hybrid"**

**Core Capabilities:**

- **🎉 NEW: Kubernetes Cost Allocation** (launching at KubeCon Nov 10, 4 days after this Summit!)
    - **Container-level cost tracking** using real in-cluster metrics
    - **Intelligent distribution** of idle capacity and shared overhead (kube-system, monitoring, networking)
    - **Universal K8s support:** EKS, AKS, GKE, OpenShift, Rancher, Tanzu, self-managed
    - **Bill-accurate allocation** including enterprise discounts and credits
    - **FOCUS-compliant** from day one—own your data, not your vendor
    - Target: **<1 hour to full visibility, 99.9% accuracy**
- **Hybrid cost normalization:** AWS, VMware, OpenShift in one FOCUS-compliant view
- **Automated chargeback workflows** with audit trails
- **AI-powered forecasting & anomaly detection** (28+ days historical)

**What This Means for BofA:**

- Taryn Thomson's CFO office **finally gets accurate Kubernetes chargeback** (industry avg: 44% of orgs can't do this)
- VG Kurup can answer "on-prem vs. AWS?" with **real TCO data, not estimates**
- Finance stops chasing mystery line items
- **Same agent** collects data for both optimization and cost allocation (no separate tools)

**Proof Point:** Lobster automated **80 hours/month** of manual chargeback work and improved TCO accuracy from **±40% to ±5%**

---

**Deployment & Time-to-Value:**

- **Week 1:** Connect AWS + one OpenShift cluster → cost visibility dashboard live
- **Weeks 2-4:** Deploy lightweight agents inside OpenShift for container-level attribution + optimization
- **Month 2:** Integrate Terraform blueprints + enable self-service catalog with governance
- **Month 3:** Full chargeback + optimization operational across hybrid

**Scalability:**

- **1B+ cost records/day** in production
- Customers managing **100,000+ resources**
- **Sub-5-minute** query response (vs. CloudHealth's 5-15s lag)

**Enterprise Integration:**

- **200+ pre-built connectors** (ServiceNow, Jira, Terraform, Ansible, all clouds)
- **Python-based extensibility** (not Groovy/Java like Morpheus)
- **Agentless** for cloud APIs | **Lightweight optional agents** for K8s/VMware metrics (non-invasive)
- **24/7 support** + dedicated Technical Success Manager
- **SOC 2 Type II**, GDPR, FedRAMP in process

---

### **SLIDE 5: Proof—Three Customers, Three Use Cases** _(REVISED)_

**Time: 6 minutes (2 min each)**

**Purpose:** Map each customer story to one of the three use cases

---

#### **Customer 1: CIGNA—Cloud Management at Scale**

_(Use Case: Orchestrator of Orchestrators)_

**Challenge:**

- 20,000+ cloud resources across AWS, Azure, VMware
- Manual provisioning via ServiceNow tickets: **3+ weeks per request**
- 40% of resources untagged → chargeback nightmare
- Security policies enforced **after deployment** (reactive cleanup, not proactive prevention)

**What CloudBolt Did:**

- Deployed unified self-service catalog with **policy-as-code** embedded in Terraform blueprints
- **Orchestrated existing Terraform modules**—didn't replace them, wrapped them with governance
- Automated tagging compliance + pre-deployment security scans
- **Integrated with ServiceNow** for approval workflows (ServiceNow = approvals, CloudBolt = orchestration)

**Results:**

- **Provisioning time: 3 weeks → 4 hours** (94% reduction)
- **Untagged resources: 40% → <5%** (automated tag enforcement)
- **Zero security violations** across 10,000+ automated deployments in first 6 months
- **$2.3M annual savings** via automated resource cleanup

**Why This Matters for BofA:** Cigna had the same challenge you do—ServiceNow + Terraform working in silos. CloudBolt became the orchestration layer so developers kept their Terraform workflows while ITOps gained **automated governance**.

---

#### **Customer 2: ACQUIA—Kubernetes Workload Optimization**

_(Use Case: Multi-Platform Optimization)_

**Challenge:**

- 200+ Kubernetes clusters across AWS EKS, GCP GKE, on-prem OpenShift
- Engineering **over-provisioned by default** because they couldn't see real utilization
- Evaluated CAST AI, CloudHealth, CloudZero—all had **data trust issues**:
    - CAST AI: 7-day lookback couldn't see monthly billing patterns
    - CloudHealth: Stale data, manual refresh cycles
    - CloudZero: Silent data gaps without notification

**What CloudBolt Did (StormForge Workload Optimization):**

- Deployed **lightweight agents inside OpenShift clusters** to capture real namespace/pod-level usage
- **ML-based rightsizing** with **28+ days historical analysis** (vs. CAST AI's 7-day limit)
- Optimized **both requests AND limits intelligently** (not CAST AI's crude 1.5x multipliers)
- **Enhanced native HPA**—didn't force replacement like CAST AI does

**Results:**

- **$2.1M annual cost reduction** (26% of Kubernetes spend)
- **Zero production incidents** from optimization changes (unlike CAST AI's forced HPA replacement)
- **"If I have to double-check the reporting tool, I don't trust it"**—Acquia chose CloudBolt for **data integrity**

**Why This Matters for BofA:** You're running OpenShift at scale. Acquia proved that **continuous Kubernetes optimization** is possible **without stability risks**—and the same pattern applies to your VMware VMs and AWS instances.

---

#### **Customer 3: LOBSTER—Hybrid Cost Allocation & Reporting**

_(Use Case: Cost Allocation Across Hybrid)_

**Challenge:**

- **4,500 customers** on multi-tenant cloud platform (70% VMware on-prem, 30% AWS)
- No unified view of AWS + VMware costs → **TCO analyses were guesswork (±40% margin of error)**
- **80+ hours/month per team** spent on manual chargeback processes
- Needed **FOCUS-compliant reporting** for investor due diligence

**What CloudBolt Did:**

- **FOCUS-native cost normalization** across AWS + VMware (FinOps Foundation Certified Platform)
- Deployed **CloudBolt agents inside VMware** to capture ground-truth utilization (not just vCenter approximations)
- Built **custom reporting in <1 hour** using Python extensibility (engineer did this **during training session**)
- Automated chargeback workflows with full audit trails

**Results:**

- **80 hours/month saved** (chargeback now fully automated)
- **VMware + AWS costs in one FOCUS-compliant view** for first time
- **TCO accuracy: ±40% → ±5%** (informed "on-prem vs. AWS" decisions with real data)
- **Python extensibility:** Custom PagerDuty + legacy ticketing integration built in 1 hour

**Why This Matters for BofA:** Lobster's hybrid challenge mirrors yours—they needed to compare VMware and AWS costs with **real utilization data, not depreciation estimates**. With your OpenShift footprint, **adding Kubernetes cost allocation** (launching Nov 10) gives you **complete hybrid visibility for the first time**.

---

**Transition to Slide 6:**  
"Those are three proof points that convergence works in production. Now let's talk specifically about what this could look like at Bank of America..."

---

### **SLIDE 6: BofA-Specific Use Case Proposals** _(REVISED)_

**Time: 3 minutes**

**Purpose:** Three concrete proposals mapping to the three use cases

**Framework:** Situation → What We'd Do → Timeline → Success Metric

---

#### **Proposal A: Unify Terraform Governance Across Hybrid**

_(Use Case: Cloud Management)_  
_(For: Ryan Haggerty [Infrastructure Architecture], Graeme Muirhead [Automation])_

**The Situation:**

- Your Terraform configs work great in AWS
- On-prem deployments still require **manual ServiceNow approvals** and lack consistent tagging
- ServiceNow integration is **custom-built**—every Terraform update requires re-coding workflows
- No unified governance layer across AWS, VMware, OpenShift

**What We'd Do:**

- **Wrap existing Terraform modules in CloudBolt blueprints** with pre-deployment policy checks (tagging, security groups, budget approvals)
- Same developer experience (they still use Terraform CLI or GitOps)
- **ServiceNow becomes approval layer, CloudBolt handles orchestration**—no more custom integration work
- **One governance model** across AWS, VMware, OpenShift

**Timeline:** 60-day pilot  
**Success Metric:**

- 100% tag compliance on new resources
- 80% reduction in manual approval bottlenecks
- Developers deploy to AWS or on-prem with **identical process**—both compliant by default

---

#### **Proposal B: Optimize Kubernetes Workloads Across OpenShift**

_(Use Case: Workload Optimization)_  
_(For: VG Kurup [Datacentre & Cloud Services], Rick Knafelz [End User & DevOps])_

**The Situation:**

- You're running ROSA on AWS + on-prem OpenShift
- Engineering **over-provisions by default** because they can't see real utilization inside clusters
- Industry average: **30% of Kubernetes spend is wasted**
- No visibility into **idle capacity** or **inefficient workloads**

**What We'd Do:**

- Deploy **StormForge agents inside OpenShift clusters** (same agent used for cost allocation)
- **ML-based rightsizing** with 28+ days historical analysis (sees monthly billing patterns)
- Optimize **requests and limits** based on actual workload behavior
- **Automated optimization** or recommendation mode (your choice)

**Timeline:** 30-day POC  
**Success Metric:**

- **15-30% reduction in Kubernetes compute costs** (based on Acquia benchmark)
- Zero production incidents from optimization changes
- Full visibility into **idle capacity** and optimization opportunities

**🎉 BONUS:** Same agent provides **container-level cost allocation** (launching Nov 10)—**solve optimization and allocation in one deployment**

---

#### **Proposal C: Kubernetes Cost Allocation Across Hybrid OpenShift**

_(Use Case: Cloud Allocation & Reporting)_  
_(For: VG Kurup [Datacentre & Cloud Services], Taryn Thomson [CFO Office])_

**The Situation:**

- You're running ROSA + on-prem OpenShift, but Finance gets **one opaque line item** for all Kubernetes spend
- **44% of companies can't allocate Kubernetes costs at workload level** (industry benchmark)
- Current state: Finance can't chargeback to business units, engineering can't identify waste
- TCO analyses for "on-prem vs. AWS" are **guesswork (±40% margin of error)**

**What We'd Do:**

- **🎉 EARLY ACCESS:** Deploy our Kubernetes Cost Allocation capability (launching publicly at KubeCon Nov 10, **4 days after this Summit**)
- **Lightweight agents inside ROSA and on-prem OpenShift** to capture real namespace/pod-level consumption
- **Bill-accurate allocation** including AWS enterprise discounts and credits
- Map costs back to business units using your existing chargeback hierarchy
- **FOCUS-compliant reporting** so OpenShift costs normalize with AWS and VMware

**Timeline:** 30-day POC (you'd be among first production deployments)  
**Success Metric:**

- Allocate **95%+ of Kubernetes costs** with full audit trail (vs. industry avg of 56%)
- CFO's office can answer **"What does Project X cost us in OpenShift?"** without guesswork
- **<1 hour to full visibility** from agent deployment
- **99.9% bill accuracy** (target)

**Why This Is Urgent:**

- Industry data: **28% of orgs report Kubernetes is 25-50% of total cloud spend**
- For BofA's scale, that's likely **tens of millions in unallocated spend annually**
- This capability **launches publicly in 4 days**—you'd get **early access and white-glove implementation support**

---

**The Ask:**  
"Which of these three would create the most immediate business value for you? Or should we explore all three in a phased approach—starting with the one that solves your biggest pain point?"

---

### **SLIDE 7: Why CloudBolt vs. Point Solutions** _(REVISED)_

**Time: 2 minutes**

**Purpose:** Crystallize the convergence value prop

**Title:** "Why Organizations at BofA's Scale Choose Convergence"

**Content:**

✅ **One Platform, Three Critical Capabilities**  
Instead of stitching together Morpheus (CMP) + CloudHealth (FinOps) + CAST AI (K8s optimization), you get **orchestration + optimization + allocation in one platform**

✅ **Orchestrates Your Investments, Doesn't Replace Them**

- We wrap Terraform with governance (don't replace it)
- We expose OpenShift costs and optimize workloads (don't replace it)
- We integrate with ServiceNow for approvals (don't replace it)

✅ **Universal Kubernetes Support**  
Unlike vendors locked to specific flavors (FinOut = AWS-heavy, CAST AI = limited distributions), CloudBolt works **identically across EKS, AKS, GKE, OpenShift, Rancher, Tanzu, self-managed**

✅ **FOCUS-Native from Day One**  
FinOps Foundation Certified Platform—own your data in industry-standard format, not vendor lock-in (unlike Kubecost's proprietary format)

✅ **ML-Powered Optimization Without Stability Risks**

- **28+ day analysis** (vs. CAST AI's 7-day lookback that misses monthly patterns)
- **Enhances native HPA** (vs. CAST AI forcing proprietary replacement)
- **Optimizes requests AND limits intelligently** (vs. CAST AI's crude 1.5x multipliers)

✅ **Same Agent, Dual Purpose**  
The lightweight agent inside Kubernetes clusters does **both cost allocation AND optimization**—deploy once, solve two problems

✅ **Python Extensibility**  
Your teams already know Python—no Groovy/Java required (Lobster built custom integration in 1 hour during training)

✅ **Enterprise-Proven in Regulated Industries**  
FedRAMP, HIPAA, financial services deployments—we understand audit trails, air-gapped environments, compliance

✅ **Predictable Commercials**  
Transparent pricing vs. CloudHealth's 2-10x renewal shocks post-Broadcom

✅ **Speed & Data Trust**

- **2-3s query times** (vs. CloudHealth's 5-15s lag)
- **No manual refresh cycles** (vs. CloudHealth's 1hr+ manual refreshes)
- Acquia's verdict: _"If I have to double-check the tool, I don't trust it"_

---

**What We're Transparent About (Roadmap vs. Today):**

- ✅ **Available Today:** CMP orchestration, FOCUS-native FinOps, Terraform/Ansible integration, VMware optimization, AWS optimization
- 🎉 **Launching Nov 10 (4 days from now):** Kubernetes Cost Allocation with StormForge integration
- 🚧 **Q1 2026 Roadmap:** AI co-pilot for blueprint creation, natural language cost queries

---

### **SLIDE 8: What Happens Next** _(Unchanged)_

**Time: 2 minutes**

**Three-Phase Approach:**

**Phase 1: Proof of Value (30 days)**

- Connect one AWS account + one OpenShift cluster
- **🎉 Early access:** Deploy Kubernetes Cost Allocation (launching Nov 10)
- Demonstrate FOCUS-compliant hybrid reporting
- **Deliverable:** Executive dashboard showing AWS + OpenShift costs with container-level visibility

**Phase 2: Pilot (60 days)**

- Integrate Terraform workflows into service catalog with governance
- Deploy workload optimization (Kubernetes + VMware or AWS)
- Onboard 2-3 business units for chargeback
- **Deliverable:** Quantified ROI (time saved, waste eliminated, governance value)

**Phase 3: Enterprise Rollout (6-12 months)**

- Scale across all clouds, all environments
- Full FinOps operationalization (forecasting, anomaly detection)
- Advanced automation (policy-driven optimization, predictive rightsizing)
- **Deliverable:** Self-sustaining platform with 24/7 support + Technical Success Manager

**Investment Framework:**  
"We're transparent: This isn't a $50K point solution. For an organization at BofA's scale, you're looking at **$300-600K annually** depending on scope. But if we can't demonstrate **10X ROI in the pilot** (time savings + waste elimination + governance value), we don't deserve the enterprise business."

**Next Steps:**

1. **Prep Call with TPD Team** (already scheduled): Refine use case proposals
2. **30-Day POC Scoping:** Propose specific technical plan for your priority use case
3. **Parallel Run Option:** Run CloudBolt alongside current tools to prove delta—no rip-and-replace

---

## **SPEAKING NOTES & KEY TRANSITIONS**

**Opening (Rod):** "We're not here to pitch you a product. We're here because we think Bank of America has three specific problems that your current foundation—Terraform, ServiceNow, OpenShift—can't solve on its own. And we've spent 13 years building a platform to solve these exact problems for enterprises at your scale. Let's see if we're right."

**Transition from Slide 2 → 3:** "These three problems—orchestration fragmentation, optimization blindness, cost opacity—weren't created by bad decisions. You built the right foundation. These are the problems that **emerge at scale** when point solutions that were never designed to work together start creating operational seams. Let me show you what I mean..."

**Transition from Slide 3 → 4:** "So that's why the alternatives break down. Now let me show you how CloudBolt solves all three problems—not with three different products, but with three converged capabilities in one platform..."

**Transition from Slide 5 → 6:** "Those are three proof points that convergence works in production—real metrics, real customers. Now, the big question: which of these patterns would create the most value for Bank of America specifically?"

**Closing (Rod):** "Here's what I believe: The next stage of hybrid cloud maturity isn't about adding more tools to your stack. It's about **converging** the capabilities you need—orchestration, optimization, allocation—into one platform. If that thesis resonates, let's explore a 30-day POC on whichever use case solves your biggest pain point. And because we're launching Kubernetes Cost Allocation in **4 days** at KubeCon, you'd get early access and white-glove support. Thank you for your time."

---

## **CRITICAL PRE-BRIEF QUESTIONS**

**Before the prep call with BofA's TPD team, confirm:**

1. **OpenShift Architecture:**
    
    - Are they running ROSA (managed), self-managed on AWS, or both?
    - On-prem OpenShift version?
    - This affects how we position K8s cost allocation deployment
2. **Kubernetes Spend Visibility:**
    
    - Does Finance currently get any OpenShift cost breakdown below cluster level?
    - If yes, how? (Manual estimates? Kubecost? Other tool?)
    - This determines our baseline for the "before" state
3. **Competitive Landscape:**
    
    - Have they evaluated CloudHealth, Morpheus, CAST AI, or Kubecost?
    - If yes, why didn't they proceed? (Avoid landmines)
4. **ServiceNow Terraform Integration:**
    
    - How mature is their current ServiceNow + Terraform workflow?
    - Custom-built or using ServiceNow's native Terraform plugin?
    - What's breaking today?
5. **FinOps Maturity:**
    
    - Do they have a dedicated FinOps team/practice?
    - Who owns chargeback today? (Finance? IT? Shared?)
    - What's their current chargeback methodology?
6. **VMware Transition Plans:**
    
    - Post-Broadcom: Are they planning to migrate off VMware?
    - Timeline? Target platforms (OpenShift, Nutanix, public cloud)?
    - This affects how we position workload optimization
7. **Pricing Envelope:**
    
    - What's realistic Year 1 deal size? ($300-600K? Higher?)
    - Procurement cycle timing?

---

## **BACKUP SLIDES (FOR Q&A—NOT IN DECK)**

**If Asked: "How does K8s Cost Allocation work technically?"**

- Lightweight agent (same one used for StormForge optimization) runs as DaemonSet in each cluster
- Collects real-time metrics: CPU/memory requests & limits, actual usage, pod lifecycles
- Maps Kubernetes resources back to cloud bill line items (EC2 instances, persistent volumes, load balancers)
- Applies intelligent allocation rules for shared costs (kube-system, monitoring, idle capacity)
- Outputs FOCUS-compliant cost data with namespace, pod, label dimensions
- Target: <1 hour from agent deployment to full visibility
- **Bill-accurate:** Includes enterprise discounts, RIs, Savings Plans

**If Asked: "What about VMware/Broadcom strategy?"**

- We're vendor-agnostic—if you stay on VMware, we support it
- If you migrate to OpenShift/Nutanix/cloud, we orchestrate it
- Many customers use CloudBolt to **de-risk Broadcom** by enabling **workload portability**
- Example: Cigna has parallel blueprints for VMware and AWS—can shift workloads based on cost/performance

**If Asked: "How is this different from Kubecost?"**

- **Universal K8s support:** Kubecost struggles with OpenShift/Rancher/Tanzu; we support all distributions identically
- **FOCUS compliance:** Kubecost locks you into proprietary data format; we output industry-standard FOCUS
- **Integrated optimization:** Kubecost shows costs; we show costs + optimization opportunities + auto-remediation
- **Hybrid view:** Kubecost is K8s-only; we unify K8s + VMware + AWS costs in one view

**If Asked: "What's the catch with 'early access'?"**

- General Availability is Q4 2025 (weeks away, not months)
- Early access means: You get it first, we provide white-glove support, you give us feedback
- No beta risk—this is production-ready code, just not publicly launched yet
- You'd be reference customer for financial services use case

---

William, this revision:

1. ✅ **Focuses on your three use cases:** Cloud Management, Workload Optimization, Cloud Allocation
2. ✅ **Emphasizes Kubernetes heavily:** Cost allocation as hero feature (launching Nov 10!)
3. ✅ **Shows same pattern applies across hybrid:** K8s + VMware + AWS
4. ✅ **Incorporates K8s Cost Allocation product details** from your doc
5. ✅ **Maps customer stories to use cases:** Cigna = CMP, Acquia = Optimization, Lobster = Allocation
6. ✅ **Maintains 8-slide structure** per BofA guidelines
7. ✅ **"Early access" positioning:** Makes the timing (4 days before KubeCon launch) feel like an advantage

**Key strategic move:** Proposal C (K8s Cost Allocation) is the **"spearhead"**—it's new, it's launching in 4 days, and it solves BofA's biggest blind spot (OpenShift cost opacity). Use that to get them in the door, then expand to CMP and optimization.

Ready to build the actual slides?

— Strat