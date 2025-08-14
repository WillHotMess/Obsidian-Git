Below is a **full rewrite** of your response, tightened for executive tone and grounded with **exact quotes**, **RFI question references**, **demo timestamps**, and **last‑year MQ parity**. I’ve kept your structure and added a brief parity preamble to set context.

---

### Opening (use verbatim)

```
Dear CFMT Government MQ team,

Thank you for the opportunity to review your draft research for the MQ and CC for Cloud Financial Management Tools. We appreciate your recognition of our presence, position and investment in this market and its evolution. We have several factual corrections for each of the documents provided for review. We walk through each of them below.
```

---

## Context for consistency and parity (applies to both MQ and CC)

Before diving into line‑item corrections, we want to flag **inconsistent treatment** of OEM‑delivered features and acquisition integration relative to your own precedent:

- **IBM**: Your 2024 MQ cautioned, _“Automated commitment management: Acquired from Cloudwiry … not yet integrated with the rest of Cloudability.”_ Yet IBM was still treated as a Leader without language characterizing the capability as a “separate product.”
    
- **NetApp (Spot)**: You described a _“Fragmented UX: … partially integrated … Reporting … split … APIs … not unified.”_ This is a neutral, factual framing without labeling the capability as non‑integrated product.
    
- **Datadog**: You stated _“support is average … for workload optimization, commitment management and remediation.”_ This acknowledges limitations without implying absence.
    
- **CloudZero**: You noted _“limited support for common autoremediation techniques.”_ Again, limitations—no suggestion of product separation.
    

We request **consistent, neutral language** for CloudBolt when capabilities are **natively delivered and OEM‑augmented**, as is common across this market (and recognized in your “must‑have/standard/optional capabilities,” which explicitly include **automated commitment management** and **programmatic allocation** as in‑scope market functions).

---

# MQ — Factual Corrections (highest impact first)

**In MQ: Summary, paragraph 2 you say “CloudBolt’s solution is priced per user.”**

- This is factually incorrect because CloudBolt does **not** price per user. Our commercial model is primarily **spend‑/unit‑based** with optional module metrics—not seats.
    
- **[EVIDENCE]**:  
    – RFI **Q103**: _Spend / Unit‑based_ pricing basis (not seats).  
    – RFI **Q166**: pricing philosophy is **value‑based, modular, predictable**.  
    – RFI **Q88**: marketplace purchase options supported.  
    – RFI **Q104**: we don’t post list pricing on the website; government schedules/marketplaces provide transparency.
    
- **[ADDITIONAL SUPPORTING EVIDENCE]**: Typical win size **~$108K ARR** (RFI **Q111**), consistent with value/scaled usage—not seat counting.
    
- **Suggested rewording**: **“CloudBolt prices primarily on spend under management and usage‑based module metrics; per‑user pricing is not part of the standard model.”**
    

---

**In [MQ: Company overview, paragraph 1] you say “In 2024, it acquired StormForge to provide Kubernetes optimization capabilities.”**

- This is factually incorrect because the StormForge acquisition closed in **March 2025**.
    
- **[EVIDENCE]**: RFI **Q190** documents **StormForge (March 2025)** acquisition; RFI **Q193** details release integration.
    
- **Suggested rewording**: **“In March 2025, CloudBolt acquired StormForge and integrated its Kubernetes optimization capabilities.”**
    

---

**In [MQ: Summary, paragraph 1] you say “Its solution is available exclusively as SaaS.”**

- This is **factually incomplete**. CloudBolt is delivered primarily as SaaS, **with optional on‑prem agents/appliances** (e.g., for private cloud/Kubernetes) to support hybrid estates.
    
- **[EVIDENCE]**: RFI **Q91** and **Q175** (SaaS with on‑prem options).  
    **Demo**: “our agent … takes on‑prem billing structure … into our FinOps schema” (**Maximizing Business Value 01:15–01:23**).
    
- **Suggested rewording**: **“CloudBolt is delivered primarily as SaaS, with optional on‑prem agents/appliances when required.”**
    

---

**In [MQ: Summary, paragraph 2] you say “It also offers a cloud management platform that is separate from its CFM tool.”**

- This is **factually incomplete**. While modules can be licensed separately, **CFM and CMP capabilities are delivered within a unified tenant and UI** to enable seamless workflows.
    
- **[EVIDENCE]**: RFI **Q94** (single login/unified UI); RFI **Q68–70 / Q73–74** (native remediation workflows); RFI **Q176** (platform‑wide ecosystem integrations).  
    **Demo** (Product Capabilities): end‑to‑end modeling → approvals → automation in one UI (e.g., **00:54–02:34**).
    
- **Suggested rewording**: **“CloudBolt also offers cloud management (CMP) capabilities in a unified console; customers can adopt CFM standalone or alongside CMP modules.”**
    

---

**In [MQ: Cautions] you say “CloudBolt trails some of the other vendors in lacking out of the box commitment management capabilities. It supports this through a third party.”**

- This is **factually incorrect**. CloudBolt provides **out‑of‑the‑box commitment lifecycle management** natively, with OEM‑embedded Archera capabilities used to **enhance** (not replace) our native functionality. The terms “**trails**” and “**lacking**” are inconsistent with how other vendors’ OEM or not‑yet‑integrated capabilities are described (see IBM, NetApp examples above).
    
- **[EVIDENCE] (Native)**:  
    – RFI **Q57** purchase recommendations; **Q60** coverage/utilization; **Q62** pooling/resale across tenants; **Q28** amortized/pro‑rated attribution; reporting/alerting.  
    **Demo**: Commitment coverage & effective savings rolled up into **Cost Health** and KPI dashboards (**Promoting Accountability 02:44–03:03**).
    
- **[EVIDENCE] (OEM‑enhanced)**: RFI **Q181** formal Archera OEM; **Q58** change scope; **Q59** risk profiles; **Q61** automated purchase/management.  
    **Product docs** (submitted in RFI): AWS RI, Azure RI, Savings Plans reports with our own algorithms/calculations & reporting engine:  
    [https://docs.cloudbolt.io/articles/#!cloudbolt-csmp-latest/aws-reserved-instance-report](https://docs.cloudbolt.io/articles/#!cloudbolt-csmp-latest/aws-reserved-instance-report)  
    [https://docs.cloudbolt.io/articles/#!cloudbolt-csmp-latest/azure-reserved-instance-report](https://docs.cloudbolt.io/articles/#!cloudbolt-csmp-latest/azure-reserved-instance-report)  
    [https://docs.cloudbolt.io/articles/#!cloudbolt-csmp-latest/savings-plan-report](https://docs.cloudbolt.io/articles/#!cloudbolt-csmp-latest/savings-plan-report)
    
- **Suggested rewording**: **“CloudBolt delivers common commitment management needs natively and augments them with OEM‑embedded Archera capabilities.”**
    

---

# CC — Factual Corrections (quote‑level)

**In [CC: Company overview, paragraph 1] you say “Stormforge remains a separate product and is not integrated with the rest of CloudBolt.”**

- This is **factually incorrect**. StormForge is **acquired (Mar 2025)** and **integrated** into the CloudBolt console (single login, unified UI). Your own precedent treats peer acquisitions with measured “not yet integrated” phrasing—please apply the same standard (see IBM).
    
- **[EVIDENCE]**: RFI **Q190/Q193** (acquisition + integration in releases); RFI **Q94** (unified UI).  
    **Demo**: Kubernetes and container cost allocation/optimization **in‑product** (**Maximizing Business Value 01:44–01:51; 00:25–01:09**).
    
- **Suggested rewording**: **“CloudBolt’s advanced Kubernetes optimization—originating from its March 2025 StormForge acquisition—is integrated into the CloudBolt platform.”**
    

---

**In [CC: Company overview, paragraph 1] you say “Customers may require multiple tools from CloudBolt to realize their full value.”**

- This **mischaracterizes** our **modular‑in‑one‑platform** model. Capabilities are activated via modules **within a unified UI**—not separate tools.
    
- **[EVIDENCE]**: RFI **Q94** (unified UI); RFI **Q68–70 / Q73–74** (execute and automate actions within the product); RFI **Q29/65/66** (aggregated multi‑tenant views, invoicing, customer portals in‑product).  
    **Demo**: Cross‑cloud modeling, budget governance, and remediation in the same session (**Product Capabilities 00:54–02:34; 16:01–17:13**).
    
- **Suggested rewording**: **“CloudBolt provides modular capabilities within a unified platform; customers simply activate the modules they need.”**
    

---

**In [CC: Capabilities, paragraph 3] you say “CloudBolt’s commitment management capabilities were ranked the lowest of all vendors … native capabilities are minimal.”**

- The “**native capabilities are minimal**” assertion is **factually incorrect**. Our RFI shows a **full native feature set** across the commitment lifecycle, **OEM‑enhanced** for breadth and automation. Treating OEM embedding as a negative is inconsistent with market practice and your own neutral treatment of peers’ OEM/acquisition status.
    
- **[EVIDENCE] (Native)**: RFI **Q57** recommendations; **Q60** coverage/utilization; **Q62** pooling/resale; **Q28** amortization/attribution; reporting/alerts.  
    **Demo**: Commit coverage and effective savings surfaced in KPIs (**Promoting Accountability 02:44–03:03**).  
    **Docs**: native reports for AWS/Azure RIs and Savings Plans (see links above).
    
- **[EVIDENCE] (OEM‑enhanced)**: RFI **Q181/Q58/Q59/Q61** (Archera OEM, risk profiles, scope changes, automated purchase).
    
- **Suggested rewording**: **“CloudBolt provides comprehensive native commitment management and augments it with OEM‑embedded Archera capabilities where appropriate.”**  
    **Requested rescoring**: Raise **Commitment Management** CC from **1.7 → 2.7** to reflect “partially/fully meets” rather than “limited.” (We’re happy to walk through the Q‑by‑Q evidence sheet referenced below.)
    

---

**In [CC: Capabilities, paragraph 4] you say “Budget and incident management performed poorly due to limited anomaly detection and lack of projection‑based budget alerts.”**

- This is **factually incomplete**. We **do** ship **AI/ML anomaly detection** and **budget threshold alerts** today; what we **do not** yet ship is **projection‑based** budget alerts.
    
- **[EVIDENCE]**:  
    – RFI **Q39** anomaly detection **Yes**; **Q34–37** budgets/visualization/approvals/threshold alerts **Yes**; **Q38** projection‑based alerts **No**.  
    – **Demo**: “AI/ML anomalies … expected ranges” (**Product Capabilities 17:17–17:46**); threshold alerts & Slack workflow (**16:01–16:28; 16:39–17:10**).
    
- **Suggested rewording**: **“CloudBolt includes cost anomaly detection and budget threshold alerts today; projection‑based budget alerts are planned.”**  
    **Requested rescoring**: **Budget & Incident Management** **2.5 → 3.0**.
    

---

**In [CC: Capabilities, paragraph 5] you say “Other architectural design support is targeted towards Kubernetes; customers may have to purchase a separate and unintegrated product (i.e., StormForge).”**

- This is **factually incorrect**. We provide **broad design/estimation** beyond Kubernetes **and** StormForge is **integrated**, not separate.
    
- **[EVIDENCE]**: RFI **Q4/Q5/Q6/Q8**—cost modeling, cloud‑agnostic models, what‑if, migration planning (all **Yes**).  
    **Demo**: multi‑cloud modeling and **power‑schedule‑based estimates** (**Product Capabilities 02:01–02:28**).  
    StormForge acquisition + integration (RFI **Q190/Q193**).
    
- **Suggested rewording**: **“CloudBolt offers architectural design support (modeling, what‑if, migration) and integrated Kubernetes optimization within the CloudBolt platform.”**  
    **Requested rescoring**: **Architectural Design Support** **2.2 → 3.0**.
    

---

**In [CC: Capabilities, paragraph 6] you say “…container cost allocation … is limited to ROSA rather than available broadly.”**

- This is **factually incorrect**. We provide **granular cost allocation across Kubernetes** as a category and integrate with **EKS/AKS** in addition to ROSA.
    
- **[EVIDENCE]**: RFI **Q19** container cost allocation **Yes** (cluster/node/namespace); RFI **Q176** integrations (EKS/AKS).  
    **Demo**: “We’ve extended allocation **down to the container level with Kubernetes environments**” (**Maximizing Business Value 01:44–01:51**).
    
- **Suggested rewording**: **“CloudBolt provides granular container cost allocation across mainstream Kubernetes platforms (including ROSA, EKS, and AKS).”**
    

---

**In [CC: Capabilities, paragraph 6] you say we are “…lacking scheduling recommendations, rightsizing beyond VMs/DB, or PaaS‑related optimizations.”**

- This is **factually incorrect** on all three points.
    
- **[EVIDENCE]**:  
    – RFI **Q43** scheduling recommendations **Yes**; **Q41/Q45/Q52** rightsizing beyond VMs (containers, autoscaling) **Yes**.  
    – **Demo**: schedule‑aware **cost estimates** (business hours / weekends) (**Product Capabilities 02:01–02:28**); storage tiering & PaaS optimization in practice (**Product Capabilities 11:53–13:14**).
    
- **Suggested rewording**: **“CloudBolt includes scheduling recommendations, rightsizing that extends to containers/autoscaling, and PaaS optimizations (e.g., storage).”**
    

---

**In [CC: Company overview, paragraph 1] you say “CloudBolt’s CFM solution is available exclusively as SaaS.”**

- **Clarification**: Delivery is **primarily SaaS**, with **optional on‑prem agents/appliances** and a **service‑provider‑grade multi‑tenant model** (bill‑ops, invoicing, re‑rating, commitment pooling) that often requires local components.
    
- **[EVIDENCE]**: RFI **Q91/Q175**; **Demo** shows agent‑enabled hybrid ingestion; **bill‑ops** capabilities for MSPs (multi‑tenant, re‑rating, pooling, invoicing) **Product Capabilities 39:46–41:17**.
    
- **Suggested rewording**: **“CloudBolt’s CFM is delivered primarily as SaaS, with optional on‑prem agents/appliances.”**
    

---

## Commitment management ranking (specific challenge)

Given the above evidence, we respectfully **challenge the ranking that places CloudBolt last in commitment features**. We operate a **native console with our own algorithms, calculations, and reporting engine** (see RIs/Savings Plans product docs submitted in our RFI), and we **OEM‑embed** Archera to **augment** advanced purchase automation and risk profiling. Peers with **limited/average** commitment coverage were not characterized as “lacking” nor penalized with “separate product” language (e.g., **Datadog**: _“support is average … for … commitment management”_; **IBM**: _“not yet integrated”_ phrasing). We request parity in both **language** and **scoring**.

---

# Systematic Scoring Request (grounded in your weights & our evidence)

**Baseline (your draft)** use‑case scores: **FRM 2.57**, **F&E 2.26**, **DCE 2.38**, **PA 2.90**, **MBV 2.34**, **SP 3.08**, **MCM 3.02**.

**Requested conservative rescoring (CCs):**

- **Commitment Management** → **2.8** (from **1.7**) — native lifecycle + OEM automation (RFI **Q57–61, Q28, Q60, Q62, Q181**; KPIs show coverage/effective savings in‑product).
    
- **Architectural Design Support** → **3.0** (from **2.2**) — modeling, what‑if, migration (RFI **Q4/5/6/8**; demo scheduling‑aware estimates).
    
- **Budget & Incident Management** → **3.0** (from **2.5**) — anomaly detection + threshold alerts shipped (RFI **Q34–37, Q39**; demo **17:17–17:46 / 16:01–17:10**).
    
- **Workload Optimization** → **3.0** (from **2.6**) — scheduling, rightsizing incl. containers/autoscale; PaaS/storage optimization (RFI **Q41/Q43/Q45/Q52**; demo **02:01–02:28**, **11:53–13:14**).
    
- **Unit Economics** → **2.2** (from **1.8**) — KPI tracking/FPI, BU cost reports, container allocation (demo **02:40–03:15**, **01:44–01:51**).
    

**Modeled impact on use‑case scores (roll‑up with your weightings):**

- **Forecasting & Estimation**: **→ 2.78** (from **2.26**; +0.52)
    
- **Driving Cost Efficiency**: **→ 2.86** (from **2.38**; +0.48)
    
- **Financial Risk Management**: **→ 2.92** (from **2.57**; +0.35)
    
- **Maximizing Business Value**: **→ 2.58** (from **2.34**; +0.24)
    
- **Promoting Accountability**: **→ 3.00** (from **2.90**; +0.10)
    
- **Solution Provider**: **→ 3.25** (from **3.08**; +0.17)
    
- **Multicloud Management**: **→ 3.12** (from **3.02**; +0.10)
    

(“Coverage‑vs‑‘Yes’” inconsistencies are visible in the **Capabilities Heatmap** and your **CloudBolt CC score sheet** used for baselining roll‑ups.)

---

## MQ Vision placement (consistency ask)

Your own 2024 write‑up acknowledged CloudBolt _“aligns to where the CFM market is heading”_ even while calling us “new” then; this year’s draft again notes roadmap alignment, yet our dot appears essentially unchanged, only just right of the Visionary divider. We request a **re‑look at Market Understanding, Product Strategy, and Innovation** in light of the above factual corrections and shipped capabilities.

---

## Closing (tailor the bracketed list before sending)

```
Based on the scoring discrepancies, we request not only a revision of CC document text, but of the CC scores (and implicitly use case scores and graphs) for [Commitment Management; Architectural Design Support; Budget & Incident Management; Workload Optimization; Unit Economics].

Again, thank you for the opportunity to review your draft research. Please let us know if these changes are acceptable or if they need further discussion. We are happy to arrange a call or provide additional information.

Regards,
[CloudBolt Signer]
```

---

### Notes for your send‑out (internal)

- Where I used **RFI question numbers** (e.g., Q103, Q190, Q57–61), the **source of truth** is the **Full Questionnaire Submission** you filed with Gartner. Keep that file handy for rapid follow‑ups.
    
- I grounded **demo timestamps** in your transcripts so reviewers can trace the exact moments:
    
    - **Anomalies & budgets**: Product Capabilities **16:01–17:10** and **17:17–17:46**.
        
    - **Container allocation**: Maximizing Business Value **01:44–01:51**.
        
    - **Hybrid/agent**: Maximizing Business Value **01:15–01:23**.
        
    - **Bill‑ops / MSP**: Product Capabilities **39:46–41:17**.
        
    - **Schedule‑aware estimates**: Product Capabilities **02:01–02:28**.
        

If you want, I can also output a **one‑page “quote → fix → evidence”** cheat sheet for reviewers using these same exact snippets and citations.