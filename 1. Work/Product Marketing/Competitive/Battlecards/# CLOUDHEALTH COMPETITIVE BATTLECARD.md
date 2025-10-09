# CLOUDHEALTH (VMWARE/BROADCOM) COMPETITIVE BATTLECARD

## COMPANY OVERVIEW

CloudHealth by VMware (now under Broadcom) is an established Cloud Cost Management and Optimization (CCMO) platform that historically held strong market share, particularly in AWS-heavy and MSP environments. Following Broadcom's acquisition of VMware in late 2023 and the subsequent transfer of go-to-market operations to Arrow Electronics in May 2024, CloudHealth faces significant market disruption and customer uncertainty.

**Key Facts:**

- **Company:** CloudHealth Technologies → Acquired by VMware (2018) → Acquired by Broadcom (2023)
- **Founded:** 2012
- **HQ:** Boston, MA (now absorbed into Broadcom structure)
- **Distribution:** Exclusive through Arrow Electronics (since May 2024)
- **Market Position:** Gartner Leader (2024), Forrester Leader (Q3 2024) - though analyst notes cite innovation concerns
- **Primary Strength:** Historical AWS expertise, established MSP channel (now disrupted)

**Critical Context:**
- Broadcom acquisition triggered mass customer re-evaluation due to price increases (reports of 2-10x hikes), partner program disruption, and support quality decline
- Arrow Electronics exclusive distribution model created support access confusion and partner friction
- 32% of VMware customers actively considering alternatives (2024 CloudBolt Industry Insights Report)
- Analyst commentary: "Broadcom's reputation threatens stunted innovation" (Forrester Wave Q3 2024)

## PRODUCT OVERVIEW

CloudHealth positions itself as a comprehensive cloud financial management platform with multi-cloud visibility, optimization recommendations, and basic FinOps capabilities. However, post-acquisition realities have created significant gaps between marketing claims and platform reality.

**Core Capabilities:**
- Multi-cloud cost visibility (AWS, Azure, GCP, OCI)
- Cost allocation via "Perspectives" and FlexOrgs
- Basic optimization recommendations
- Budget tracking and alerting
- Commitment management (RIs, Savings Plans)
- MSP billing and multi-tenancy
- CloudHealth Secure State (security/compliance - may be unbundled)

**Architectural Notes:**
- SaaS-only delivery model
- AWS-centric architecture extended to other clouds
- Limited private cloud support (no native VMware FinOps despite parent company)
- No native Infrastructure as Code (IaC) integration
- Lacks FOCUS data standard adoption

**Documented Limitations:**
- **Multi-Cloud Imbalance:** "Cloudhealth is great if you're AWS primary. If you have any need for GCP or Azure functions, you're not gonna get everything you need" (Reddit user feedback)
- **Reporting Constraints:** Perspectives "severely limited in size," handling only "a few hundred objects" - unusable for large cloud estates (Gartner Peer Insights)
- **Allocation Gaps:** No virtual tagging support, no shared cost allocation mechanisms (Gartner Peer Insights, 10+ year user)
- **Limited Automation:** Scored 6.9-8.6 on automation vs. competitors scoring 9+ (G2 comparisons)

## PRICING
CloudHealth's pricing model is opaque, complex, and has become a major competitive vulnerability post-Broadcom acquisition.

**Licensing Model:**
- Percentage of managed cloud spend (historical model)
- High minimum commitments ($45K+ annual minimums cited)
- Tiered pricing with volume discounts
- No transparent public pricing - requires sales quotes
- Overage charges for spend exceeding commitments (~$0.03 per dollar cited)

**Post-Broadcom Pricing Reality:**
- **Massive Price Increases:** Reports of 2x to 10x price hikes post-acquisition
- **Example:** Beeks Group reported "tenfold increase in licensing costs"
- **Example:** Computershare quoted "10-15x" renewal pricing
- **Forced Model Changes:** Elimination of perpetual licenses, mandatory subscription shift
- **Lost Flexibility:** Existing perpetual licenses not portable to cloud environments
- **Vague Future Pricing:** Partners report pricing is "vague and subject to potential increases"

**Hidden Costs:**
- Implementation and customization services
- Premium support tiers
- Training requirements due to platform complexity
- Potential mandatory service bundles
- Technical expertise needed for Groovy/Java extensions

**TCO Factors:**

- High initial licensing cost
- Significant training investment (steep learning curve)
- Ongoing management overhead (complex reporting)
- Support quality decline increasing internal troubleshooting time
- Risk of future price escalations under Broadcom

## LANDMINES

|LANDMINE|REASON|
|---|---|
|**BROADCOM ACQUISITION CHAOS**|Unprecedented price increases (2-10x), mass talent exodus, partner program termination, support degradation - creating customer exodus|
|**ARROW EXCLUSIVE DISTRIBUTION**|Support channel confusion, indirect customer relationships, mandatory distributor lock-in, MSP partner disruption|
|**INNOVATION STAGNATION**|"Broadcom's reputation threatens stunted innovation" (Forrester). Platform hasn't kept pace with competitors in PaaS optimization, cloud financial planning, unit economics|
|**AWS DEPENDENCY**|"Great if you're AWS primary" but significant feature gaps in Azure/GCP. Multi-cloud reporting "not that great"|
|**REPORTING LIMITATIONS**|Perspectives limited to "a few hundred objects," unusable for large estates. Lacks "essential reporting capabilities" for mature organizations|
|**COST ALLOCATION GAPS**|No virtual tagging, no shared cost splitting, no mechanism for Kubernetes idle capacity attribution at workload level|
|**NO IAC INTEGRATION**|Cannot forecast cost impact before deployment, missing critical "shift left" capability for modern DevOps workflows|
|**SUPPORT QUALITY COLLAPSE**|"Actual worst" support experience (Gartner review). Post-acquisition quality decline across multiple customer reports|
|**PLATFORM COMPLEXITY**|Steep learning curve limits adoption beyond finance teams. G2 scores: 8.3 ease of use vs. competitors at 9.1-9.3|
|**NO FOCUS ADOPTION**|Not built on industry standard FOCUS specification, requiring custom normalization vs. CloudBolt's native FOCUS architecture|

## WHY WE WIN

**Key Advantages Over CloudHealth:**

### ✓ **Organizational Stability & Partnership**

- **Predictable Pricing:** Transparent, consistent pricing model vs. CloudHealth's 2-10x surprise increases
- **Direct Relationships:** No forced distributor middleman; direct support and partnership vs. Arrow gatekeeping
- **Consistent Roadmap:** Active innovation with clear product direction vs. Broadcom's cost-extraction focus
- **Vendor Independence:** Not tied to hardware sales agenda or acquisition cost recovery
- **Proof Point:** "We were surprised at how few vendors offer both comprehensive infrastructure cost management together with automation and even governance capabilities. I wanted a single solution." - Phil Redmond, Data#3

### ✓ **True Multi-Cloud Parity**

- **FOCUS-Native Architecture:** Ground-up build on industry standard vs. CloudHealth's AWS-extended architecture
- **Consistent Features:** Same capabilities across AWS, Azure, GCP, VMware, Nutanix, OpenStack vs. CloudHealth's AWS bias
- **Hybrid Cloud Excellence:** Native private cloud support (VMware, Nutanix) through FOCUS vs. CloudHealth's public cloud limitation
- **Proof Point:** "My strategy is multi-cloud so I knew I was going to need something that was going to sit above all the clouds and all the tools." - Jeff Farinich, New American Funding

### ✓ **Advanced Cost Allocation**

- **No Perspective Limits:** Unlimited allocation scenarios vs. CloudHealth's "few hundred objects" constraint
- **Virtual Tagging:** Create business contexts beyond provider tags vs. CloudHealth's lack of virtual tagging
- **Shared Cost Splitting:** Usage-based, proportional, or custom algorithms vs. CloudHealth's documented gap
- **Container-Level Attribution:** Kubernetes idle capacity allocated to workloads vs. node-level aggregation
- **Proof Point:** "The CloudBolt platform is incredibly user-friendly and intuitive, especially when it came to creating detailed cost allocation dashboards." - Direct customer feedback

### ✓ **Continuous Optimization (Not Just Recommendations)**

- **Automated Remediation:** Cloud Native Actions framework executes optimization vs. CloudHealth's recommendations-only
- **ML-Powered K8s Optimization:** StormForge acquisition delivers 40-60% K8s savings with performance guarantees
- **Private Cloud Optimization:** Agent-based VMware/OpenStack waste elimination vs. CloudHealth's public cloud focus
- **Policy-Driven Automation:** Codify manual processes into automated workflows vs. manual ticket-based remediation
- **Proof Point:** 70% average cost reduction for non-prod workloads; 15 minutes from recommendation to remediation

### ✓ **Engineer-Friendly Adoption**

- **Intuitive UI:** G2 scores show superior ease of use vs. CloudHealth's complexity
- **Faster Time-to-Value:** 15 minutes to first insight with OOTB dashboards vs. weeks of configuration
- **IaC Integration:** Pre-deployment cost forecasting in Terraform/Ansible workflows vs. CloudHealth's lack of IaC integration
- **Broad Adoption:** Self-service capabilities drive engineering engagement vs. finance-only tool usage
- **Proof Point:** "CloudBolt is transforming the way we manage our cloud resources by simplifying our automation and orchestration tasks" - Cory Moore, BeyondTrust

### ✓ **Superior Support & Implementation**

- **Responsive Support:** Consistently high support ratings vs. CloudHealth's "actual worst" post-acquisition support
- **Faster Implementation:** 80% out-of-box functionality vs. complex CloudHealth setup requiring specialized skills
- **Python Extensibility:** IT teams use familiar languages vs. CloudHealth's Groovy/Java requirement
- **Direct Access:** No distributor gatekeeping; direct technical success managers
- **Proof Point:** G2 Quality of Support - CloudBolt strengths vs. CloudHealth's declining ratings

### ✓ **Future-Proof Architecture**

- **FOCUS Foundation:** Native support for emerging standard vs. CloudHealth's proprietary data model
- **Active Innovation:** AI/ML forecasting, anomaly detection, unit economics development vs. deprioritized R&D
- **Unit Economics Ready:** Building blocks in place for cost-per-transaction analytics vs. CloudHealth's limitations
- **FinOps Performance Index™:** Proprietary maturity scoring measuring outcomes vs. basic spend metrics

## WHY WE LOSE

**Scenarios Where CloudHealth May Win:**

### • **Existing CloudHealth Entrenchment**

- Organizations with 5+ years of CloudHealth investment and extensive customization
- Significant sunk costs in training, custom dashboards, and established workflows
- Risk-averse teams unwilling to disrupt status quo despite pricing/support issues
- **Counter:** Position as modernization opportunity; emphasize CloudHealth's declining trajectory and uncertainty

### • **Pure AWS Shops**

- Organizations 90%+ AWS with no multi-cloud or hybrid strategy
- Simple use cases where CloudHealth's AWS strength still adequate
- Limited need for advanced features like shared cost allocation or K8s optimization
- **Counter:** Highlight AWS native tools (Cost Explorer) may be sufficient; CloudHealth premium not justified

### • **MSP Existing Commitments**

- Service providers with multi-year CloudHealth contracts not yet expired
- MSPs who've built proprietary integrations and customer portals on CloudHealth APIs
- Partners already migrated to Arrow distribution model
- **Counter:** Position for future renewal; plant seeds about support decline, pricing risk, limited innovation

### • **"Wait and See" Posture**

- Organizations hoping Broadcom situation stabilizes
- Belief that Arrow distribution will improve over time
- Waiting for completion of product consolidation/rebranding
- **Counter:** Show evidence of continued deterioration; opportunity cost of delayed action

### • **Budget Constraints Despite TCO**

- Ironically, some locked into CloudHealth by inability to fund migration despite higher long-term costs
- Budgets already committed to CloudHealth renewals
- **Counter:** ROI analysis showing migration payback period; financing options

## WEAKNESSES

### **Critical CloudHealth Vulnerabilities:**

### **Strategic & Organizational Weaknesses**

**Post-Acquisition Instability**

- **Mass Talent Exodus:** Key engineers and support staff leaving post-HPE, creating knowledge gaps and reduced product expertise
- **Development Stagnation:** Gartner: "VMware Tanzu CloudHealth has not kept pace in recent years with other vendors in terms of new features"
- **Customer Attrition:** 32% of VMware customers actively considering alternatives; documented migrations from major accounts
- **Partner Ecosystem Collapse:** All reseller agreements terminated; "invite-only" model restricting channel reach
- **Strategic Misalignment:** Broadcom focused on private cloud future; CloudHealth is public/multi-cloud tool
- **Proof Point:** "HP bought it and it looks like that product got gutted" - 1ITZ Prospect

**Arrow Distribution Problems**

- **Support Access Chaos:** In-platform ticketing disappeared; users redirected to "chaotic" Broadcom portal then to Arrow
- **Indirect Relationship:** GTM/support separated from product engineering, slowing feedback loop and issue resolution
- **Partner Friction:** Mandatory Arrow engagement disrupts existing MSP relationships and workflows
- **Reduced Choice:** Single distributor dependency; no alternatives if Arrow relationship problematic

**Commercial Disadvantages**

- **Opaque Pricing:** Complex WE model, no public pricing, unpredictable renewal costs
- **Extreme Price Increases:** Documented 2-10x price hikes; Beeks: "tenfold increase"; Computershare: "10-15x renewal"
- **License Model Changes:** Perpetual licenses eliminated; forced subscription migration; no cloud portability for existing licenses
- **High TCO:** List price + implementation + training + management overhead + support issues + future price risk
- **Revenue Leakage:** Even discovered/unmanaged resources count toward licensing

### **Technical & Functional Weaknesses**

**Multi-Cloud Capability Gaps**

- **AWS Dependency:** "Great if you're AWS primary. If you have any need for GCP or Azure functions, you're not gonna get everything you need"
- **Uneven Feature Parity:** Tagging, compliance, optimization work differently or less effectively on Azure/GCP vs. AWS
- **Poor Multi-Cloud Reporting:** "Not that great" - cannot provide integrated cross-cloud comparison without separate reports/views
- **No Private Cloud Support:** Zero native VMware/Nutanix FinOps despite VMware ownership - ironic and inexplicable gap

**Reporting & Allocation Deficiencies**

- **Perspective Limitations:** "Severely limited in size," only handles "a few hundred objects" - unusable for large cloud estates
- **Limited Customization:** "Not that great" reporting; complex to create custom reports requiring specialized knowledge
- **No Virtual Tagging:** Cannot group costs beyond native provider tags - major limitation for business attribution
- **No Shared Cost Allocation:** Cannot split shared resources (load balancers, K8s clusters, databases) to teams/projects
- **Container Allocation Gaps:** Idle K8s capacity not attributed at workload level, hiding optimization opportunities
- **No KPI Definition:** Cannot define KPIs beyond overall budget, limiting value-based reporting
- **Proof Point:** "Lacks essential reporting capabilities" for mature organizations - 10+ year user, Gartner Peer Insights

**Integration & Modern Workflow Gaps**

- **No IaC Integration:** Cannot forecast cost impact before Terraform/CloudFormation deployment - missing "shift left" capability
- **Limited Automation Depth:** G2 scores 6.9-8.6 vs. competitors at 9+; recommendations not execution
- **Weak Kubernetes Support:** Basic capabilities vs. specialized tools like IBM/Kubecost or CloudBolt/StormForge
- **No Unit Economics:** Cannot calculate cost-per-transaction or cost-per-customer due to allocation limitations
- **API Limitations:** Complex, potentially restrictive APIs vs. competitors' flexible, open approaches

**Platform Usability Issues**

- **Steep Learning Curve:** Complex, not intuitive, extensive training required
- **Limited Adoption:** Often used by 1-2 finance specialists; engineers don't engage due to complexity
- **Poor Engineer Experience:** UI difficult for non-financial users; doesn't support DevOps workflows
- **G2 Ease of Use:** 8.3 vs. competitors at 9.1-9.3
- **Proof Point:** "We just weren't using it" - primary reason for customer migrations

**Optimization & Remediation Weaknesses**

- **Recommendations-Only:** "Provides limited remediation actions out of the box; mostly expects user to implement"
- **Low-Quality Recommendations:** "OK, but not that great, particularly for Azure" - scores 7.8 vs. competitors 8.8-8.9
- **Outdated Recommendations:** Reports of defaulting to older, less cost-effective instance types
- **No Native Automation:** No built-in remediation execution; requires external tools or manual implementation
- **Limited Kubernetes Optimization:** Basic vs. ML-driven, workload-aware optimization from specialized vendors

**Support & Customer Experience**

- **Support Quality Collapse:** "Actual worst" support experience (Gartner review); "significantly degraded post-acquisition"
- **Access Problems:** Support ticketing removed from platform; confusion about Arrow vs. Broadcom channels
- **Declining Responsiveness:** Multiple reports of slower response times and reduced expertise
- **G2 Support Scores:** 9.0 vs. competitors at 9.1-9.5
- **Proof Point:** Multiple forum posts and reviews documenting post-acquisition support deterioration

**Architecture & Innovation Gaps**

- **No FOCUS Adoption:** Not built on industry standard data specification, requiring custom normalization
- **Legacy Architecture:** AWS-centric design extended to other clouds vs. true multi-cloud-native architecture
- **Limited PaaS/Serverless:** Weak optimization for cloud-native services vs. traditional IaaS strength
- **Stagnant Innovation:** Forrester: "Broadcom's history of limiting R&D and innovation will extend to VMware acquisition"

## PROOF POINTS

### **Analyst Assessments**

**Gartner Magic Quadrant for CFM Tools 2024:**

- "VMware Tanzu CloudHealth has not kept pace in recent years with some of the other vendors solutions evaluated in this research in terms of new features, such as cost optimization for cloud-native PaaS services and cloud financial planning"
- User review (10+ years): Lacks "essential reporting capabilities"; no virtual tagging or shared cost allocation

**Forrester Wave CCMO Q3 2024:**

- "Broadcom's reputation threatens stunted innovation"
- "Although the current roadmap promises market-leading capabilities, customers fear that Broadcom's history of limiting R&D and innovation will extend to its VMware acquisition"
- Tracy Woo: CloudHealth innovation "deprioritized under Broadcom"

**2024 CloudBolt Industry Insights Reality Report:**

- 32% of VMware customers actively considering leaving platform
- Increased costs and rigid contract terms driving churn

### **Customer Quotes & Evidence**

**Price Increase Documentation:**

- "Tenfold increase in licensing costs" - Beeks Group (moving 20,000 VMs away)
- "10-15x" renewal pricing - Computershare CTO (migrating 24,000 VMs to Nutanix)
- "2x to 268%" price hike examples documented across customer base

**Technical Limitations:**

- "Cloudhealth is great if you're AWS primary. If you have any need for GCP or Azure functions, you're not gonna get everything you need" - Reddit/FinOps forum
- "Perspectives severely limited in size, capable of handling only a few hundred objects" - Gartner Peer Insights review
- "Lacks essential reporting capabilities," no virtual tagging, no shared cost allocation - 10+ year user, Gartner
- "Multi-cloud reporting not that great" - Multiple user reports

**Support Quality:**

- "Actual worst" support experience - Gartner Peer Insights review
- "Overpriced with potentially the worst support" - Gartner review
- Support channel confusion post-Arrow transition documented across user forums

**Organizational Concerns:**

- "HP bought it and it looks like that product got gutted" - 1ITZ Prospect
- "They can't continue to grow with Morpheus" - Leidos (applicable parallel to CloudHealth situation)

### **CloudBolt Win Examples**

**Documented CloudHealth Displacements:**

- **BeyondTrust:** Migrated from CloudHealth after 8 years; "CloudBolt is transforming the way we manage our cloud resources"
- **Data#3:** "We were surprised at how few vendors offer both comprehensive infrastructure cost management together with automation"
- **Multiple Named Accounts:** Organizations switching due to Broadcom acquisition impacts, pricing concerns, and support degradation

**G2 Comparative Scores:**

- **Ease of Use:** CloudHealth 8.3 vs. competitors 9.1-9.3
- **Ease of Setup:** CloudHealth unspecified vs. Finout 8.5, Vantage 9.3
- **Quality of Support:** CloudHealth 9.0 vs. Finout 9.1, Vantage 9.4, Spot 9.5
- **Automation:** CloudHealth 6.9-8.6 vs. competitors typically 9+

### **Market Evidence**

**Customer Exodus Pattern:**

- Rackspace: Testing migration of 3,000 VMs
- Beeks Group: Moving 20,000+ VMs
- Computershare: Migrating 24,000 VMs
- Multiple Fortune 500 companies in active evaluation/migration

**Partner Disruption:**

- All reseller agreements terminated; partners required to reapply
- "Invite-only" partner program reducing market reach
- High revenue thresholds excluding smaller MSPs
- Cloud service provider agreements terminated

**Competitive Gains:**

- nOps: Ranked #1 with five stars in G2's cloud cost management category
- CloudZero: Leading in unit economics and shift-left practices
- Harness: "Market-leading innovation" recognition
- IBM: "Most complete full-stack CCMO solution" (Forrester)

## CONCLUSION

CloudHealth, historically a market leader in cloud cost management, now represents one of the most vulnerable competitive positions in the FinOps landscape. The combination of Broadcom's acquisition disruption, Arrow's exclusive distribution model, mass price increases, deteriorating support quality, and documented innovation stagnation has created an unprecedented opportunity for displacement.

**The Perfect Storm:**

- **Organizational chaos:** Talent exodus, partner program collapse, uncertain strategic direction
- **Commercial toxicity:** 2-10x price increases, eliminated licensing options, unpredictable renewals
- **Technical stagnation:** No FOCUS adoption, AWS-centric limitations, reporting gaps, allocation deficiencies
- **Support collapse:** "Worst support" experiences, Arrow gatekeeping, declining responsiveness
- **Customer flight:** 32% actively seeking alternatives; documented migrations from major accounts

**CloudBolt's Competitive Position:**

CloudBolt wins against CloudHealth by offering what customers desperately need right now:

1. **Stability & Predictability:** Transparent pricing, direct relationships, consistent roadmap
2. **True Multi-Cloud Parity:** FOCUS-native architecture with genuine hybrid cloud support
3. **Advanced Capabilities:** Shared cost allocation, virtual tagging, container-level attribution, IaC integration
4. **Action Over Analysis:** Continuous optimization with automated remediation vs. recommendations-only
5. **Superior Experience:** Engineer-friendly UI, faster time-to-value, responsive support

**Battle Strategy:**

**Awareness Stage:** Lead with Broadcom acquisition impacts - price increases, support issues, innovation concerns. Validate their pain; show you understand their uncertainty.

**Consideration Stage:** Demonstrate CloudBolt's technical superiority in their specific pain areas - allocation accuracy, multi-cloud consistency, K8s optimization, automation depth.

**Decision Stage:** Provide migration path, ROI analysis showing payback period, customer references from similar transitions. Emphasize risk of staying vs. predictable path forward with CloudBolt.

**Key Talking Points:**

- "CloudHealth's 2-10x price increases aren't a one-time event - they're the new normal under Broadcom"
- "Your CloudHealth costs will only increase while innovation decreases - that's the Broadcom playbook"
- "We're seeing unprecedented CloudHealth displacement - don't be the last one making the switch"
- "CloudHealth can show you waste; CloudBolt eliminates it automatically"
- "FOCUS-native architecture means you're future-proof, not locked into proprietary data models"

The CloudHealth opportunity is immediate and substantial. Every interaction should reinforce that staying with CloudHealth means accepting higher costs, declining support, and diminishing value - while CloudBolt offers stability, innovation, and partnership in an uncertain market.