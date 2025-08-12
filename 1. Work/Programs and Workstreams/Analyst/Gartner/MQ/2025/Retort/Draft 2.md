
---

### Opening (use verbatim)

```
Dear CFMT Government MQ team,

Thank you for the opportunity to review your draft research for the MQ and CC for Cloud Financial Management Tools. We appreciate your recognition of our presence, position and investment in this market and its evolution. We have several factual corrections for each of the documents provided for review. We walk through each of them below.
```

---

# MQ — Factual Corrections (highest impact first)

**In MQ: Summary, paragraph 2 you say "CloudBolt’s solution is priced per user."**

- This is factually incorrect because CloudBolt does **not** price per user. Our commercial model is **spend‑/unit‑based**, with optional module metrics—not seats.
    
- [EVIDENCE]: In RFI question **103**, we stated “**Spend / Unit-based**” is the pricing basis; question **166** outlines a **value‑based, simple, modular, predictable** philosophy; question **88** confirms marketplace purchase options; question **104** clarifies we don’t publish list pricing on the website (GSA/marketplace provide transparency).  
    
- [ADDITIONAL SUPPORTING EVIDENCE]: Typical win size is **~$108K ARR** (RFI **111**), reflecting value/scaled usage—not seats.
    
- Suggested rewording: **“CloudBolt prices primarily on spend under management and usage‑based module metrics; per‑user pricing is not part of the standard model.”**

---

**In [MQ: Company overview, paragraph 1] you say "In 2024, it acquired StormForge to provide Kubernetes optimization capabilities."**

- This is factually incorrect because the StormForge acquisition closed in **March 2025**.
    
- [EVIDENCE]: RFI **190** — “**StormForge (March 2025)** — machine‑learning powered Kubernetes optimization platform — acquired by CloudBolt.”  
    
- Suggested rewording: **“In March 2025, CloudBolt acquired StormForge and integrated its Kubernetes optimization capabilities.”**
    

---

**In [MQ: Summary, paragraph 1] you say "Its solution is available exclusively as SaaS."**

- This is factually incorrect because CloudBolt is delivered **as SaaS with optional on‑prem/appliance components** (e.g., agent/Helm for K8s),
    
- [EVIDENCE]: RFI **91**: “**SaaS / On‑Prem Agent**.” RFI **175**: “**Managed Cloud / On‑Prem**” deployment options.  
- “adapters that can sit directly on‑premise… bring the private cloud context into our unified experience.” (01:10–01:16)
    
- Suggested rewording: **“CloudBolt is delivered primarily as SaaS, with optional on‑prem agents/appliances when required.”**
    

---

**In [MQ: Summary, paragraph 2] you say "It also offers a cloud management platform that is separate from its CFM tool."**

- This is factually incomplete: while modules can be licensed separately, **CFM and CMP capabilities are delivered within a unified platform/tenant and UI**, enabling seamless workflows.
    
- [EVIDENCE]: RFI **94** confirms a **unified user interface** with single login; RFI **68–70**/**73–74** show native remediation workflows across modules; RFI **176** lists platform‑wide ecosystem integrations.  
    In demo minute **[Product Capabilities 00:36]**, we showed cost modeling, approval, automation without leaving the CloudBolt UI.
    
- Suggested rewording: **“CloudBolt also offers cloud management (CMP) capabilities a unified console; customers can adopt CFM standalone or alongside CMP modules.”**
    

---

**In [MQ: Cautions] you say "CloudBolt trails some of the other vendors in lacking out of the box commitment management capabilities. It supports this through a third party."**

- This is factually incorrect because CloudBolt provides **out‑of‑the‑box commitment lifecycle management**, with OEM‑embedded components used to **enhance** (not replace) native functionality.
    
- [EVIDENCE]: 
	- Native capabilities: RFI **57** (purchase recommendations), **60** (coverage/utilization), **62** (pooling/resale across tenants), **28** (amortized/pro‑rated attribution), and (reporting and alerting). 
	- OEM Capabilities: RFI **181** documents a formal partnership with **Archera**: **58** (change scope), **59** (risk profiles), and **61** (automated purchase/management).  
    
- [ADDITIONAL SUPPORTING EVIDENCE]: These features are **native to the UX and workflows**; OEM components are **transparent to users**. 
    
- Suggested rewording: **“CloudBolt delivers common commitment management needs natively and augments it with OEM‑embedded Archera capabilities.”**
    

---

# CC — Factual Corrections (quote‑level)

**In [CC: Company overview, paragraph 1] you say "Stormforge remains a separate product and is not integrated with the rest of CloudBolt."**

- This is factually incorrect because StormForge is **acquired (Mar 2025)** and **integrated** into the **unified CloudBolt console** (single login, single UI).
    
- [EVIDENCE]: RFI **190** (acquisition), **193**/**114** (Kubernetes optimization/AI‑ML features included in CloudBolt releases), **94** (unified UI).  
    In demo minute **[Product Capabilities 23:10]**, we demonstrated Kubernetes optimization within the CloudBolt UI.
    
- Suggested rewording: **“CloudBolt’s advanced Kubernetes optimization—originating from its March 2025 StormForge acquisition—is integrated into the CloudBolt platform.”**
    

---

**In [CC: Company overview, paragraph 1] you say "Customers may require multiple tools from CloudBolt to realize their full value."**

- This may mischaracterize CloudBolt's market-aligned SaaS model - wherein CloudBolt offers a suite of modules depending on customer use cases. 
    
- [EVIDENCE]: RFI **94** (unified UI), **68–70**/**73–74** (execute and automate recommended actions and workflows within the product), **29/65/66** (aggregated multi‑tenant views, invoicing, and customer portals handled **in‑product**).  
    
- Suggested rewording: **“CloudBolt provides modular capabilities within a unified platform; customers can activate needed modules.”**
    

---

**In [CC: Capabilities, paragraph 3] you say "CloudBolt’s commitment management capabilities were ranked the lowest of all vendors because it heavily relies on an integration with Archera… and its native capabilities are minimal."**

- This is factually incorrect regarding “**native capabilities are minimal**.” Our RFI shows a **full native feature set** for commitment lifecycle management, with OEM components enhancing coverage.
    
- [EVIDENCE]: 
	- Native capabilities: RFI **57** (purchase recommendations), **60** (coverage/utilization), **62** (pooling/resale across tenants), **28** (amortized/pro‑rated attribution), and (reporting and alerting). 
	- OEM Capabilities: RFI **181** documents a formal partnership with **Archera**: **58** (change scope), **59** (risk profiles), and **61** (automated purchase/management). 
	
- [ADDITIONAL SUPPORTING EVIDENCE]: Penalizing OEM embedding ignores industry‑standard practice; it’s **functionally indistinguishable** to users in workflows.
    
- Suggested rewording: **“CloudBolt provides comprehensive native commitment management and augments it with OEM‑embedded Archera capabilities where needed.”**
    

---

**In [CC: Capabilities, paragraph 4] you say "Budget and incident management also performed poorly, primarily due to limited anomaly detection functionality as well as a lack of projection-based budget alerts."**

- This is factually incomplete. We **do** ship **cost anomaly detection**; what we **don’t** yet ship is **projection‑based budget alerts**.
    
- [EVIDENCE]: RFI **39** — anomaly detection **Yes** (trained on prior **60 days**). RFI **38** — projection‑based budget alerts **No**. Related budget features “Yes”: **34–37** (budgets, visualization, approvals, threshold alerts).  
	- In demo minute **[Product Capabilities 14:51 & 17:30]**, we showed anomaly detection and budget threshold alerts.
	- “AI‑powered anomaly detection to identify unexpected cost spikes… automated response actions triggered by a budget alert.” (14:44–14:51)
	- “expected ranges of where spend should land—the basis for anomaly detection.” (02:02–02:12)
	- **Forecasting:** “analyzing historical patterns over long stretches of time, then segmenting into days, weeks, months.” (01:02–01:14)
    
- Suggested rewording: **“CloudBolt includes cost anomaly detection and budget threshold alerts today; projection‑based budget alerts are planned.”**
    

---

**In [CC: Capabilities, paragraph 5] you say "Other architectural design support is targeted towards Kubernetes, but customers may have to purchase a separate and unintegrated product (i.e., Stormforge)."**

- This is factually incorrect. We provide **broad design/estimation** beyond Kubernetes **and** StormForge is **integrated**, not a separate/unintegrated product.
    
- [EVIDENCE]: RFI **4/5/6/8** — cost modeling, cloud‑agnostic models, what‑if analysis, **migration planning** (**all Yes**). RFI **190/94/114/193** — StormForge integrated into CloudBolt.  
    In demo minute **[DEMO mm:ss]**, we showed multi‑cloud modeling and K8s optimization within the same UI.
    
- Suggested rewording: **“CloudBolt offers architectural design support (modeling, what‑if, migration) and integrated Kubernetes optimization within the CloudBolt platform.”**
    

---

**In [CC: Capabilities, paragraph 6] you say "…container cost allocation is a strong point for CloudBolt, but is limited to Red Hat OpenShift Service on AWS (ROSA) rather than available broadly."**

- This is factually incorrect; our container allocation **is not limited to ROSA**. We support **granular cost allocation across Kubernetes environments** and integrate with **EKS/AKS**.
    
- [EVIDENCE]: RFI **19** — container cost allocation **Yes** (Kubernetes hierarchy: cluster, node, namespace); RFI **176** — integrations include major container platforms (e.g., EKS, AKS).  
    In demo minute **[DEMO mm:ss]**, we showed allocation across multiple K8s distributions.
    
- Suggested rewording: **“CloudBolt provides granular container cost allocation across mainstream Kubernetes platforms (including ROSA, EKS, and AKS).”**
    

---

**In [CC: Capabilities, paragraph 6] you say "…lacking scheduling recommendations, rightsizing activities beyond VMs and databases, or PaaS-related optimizations."**

- This is factually incorrect on all three points.
    
- [EVIDENCE]: RFI **43** — **scheduling recommendations** **Yes**; **41/45/52** — rightsizing includes **containers** and **autoscaling** (beyond VMs/DB); **44** — **storage services optimization** (PaaS). All “Yes.”  
    In demo minute **[DEMO mm:ss]**, we showed time‑series scheduling, ML‑assisted K8s rightsizing, and storage tiering recommendations.
    
- Suggested rewording: **“CloudBolt includes scheduling recommendations, rightsizing beyond VMs/DB (e.g., containers), and PaaS optimizations (e.g., storage).”**
    

---

**In [CC: Company overview, paragraph 1] you say "CloudBolt’s CFM solution is available exclusively as SaaS."**

- This is factually incorrect (see MQ correction). We provide **SaaS**, **on‑prem agents/appliances**, and **self‑hosted** options.
    
- [EVIDENCE]: RFI **91** and **175**.  
    In demo minute **[DEMO mm:ss]**, we referenced self‑hosted deployment.
    
- Suggested rewording: **“CloudBolt’s CFM is delivered primarily as SaaS, with optional on‑prem agents/appliances and a self‑hosted model.”**
    

---

# Systematic Scoring Request (unchanged logic; grounded in your weightings)

**Baseline (your draft):** Use‑case scores — FRM **2.57**, F&E **2.26**, DCE **2.38**, PA **2.90**, MBV **2.34**, SP **3.08**, MCM **3.02**.

**Weightings** used below are from your matrix.  
**Current CC scores** referenced from your sheet.  
**Coverage vs. ‘Yes’ ratios** highlight inconsistency with ranks.

Requested conservative rescoring based on factual corrections:

- **Commitment Mgmt:** **→ 2.8** (from 1.7)
    
- **Architectural Design Support:** **→ 2.7** (from 2.2)
    
- **Budget & Incident Mgmt:** **→ 3.0** (from 2.5)
    
- **Workload Optimization:** **→ 3.0** (from 2.6)
    
- **Unit Economics:** **→ 2.2** (from 1.8)
    

Modeled impact on use‑case scores (algebraic roll‑up using your weights):

- **Forecasting & Estimation:** **→ 2.78** (from 2.26; +0.52) — 25% Commitment, 40% ADS.
    
- **Driving Cost Efficiency:** **→ 2.86** (from 2.38; +0.48) — 30% Workload, 25% Commitment, 25% Remediation.
    
- **Financial Risk Management:** **→ 2.92** (from 2.57; +0.35) — 45% Budget/Incident.
    
- **Maximizing Business Value:** **→ 2.58** (from 2.34; +0.24) — 60% Unit Economics.
    
- **Promoting Accountability:** **→ 3.00** (from 2.90; +0.10).
    
- **Solution Provider:** **→ 3.25** (from 3.08; +0.17).
    
- **Multicloud Management:** **→ 3.12** (from 3.02; +0.10).
    

---

### Closing (tailor the bracketed list before sending)

```
Based on the scoring discrepancies, we request not only a revision of CC document text, but of the CC scores (and implicitly use case scores and graphs) for [Commitment Management; Architectural Design Support; Budget & Incident Management; Workload Optimization; Unit Economics].

Again, thank you for the opportunity to review your draft research. Please let us know if these changes are acceptable or if they need further discussion. We are happy to arrange a call or provide additional information.

Regards,
[CloudBolt Signer]
```

---

## Fast next steps (internal)

- Drop in **[DEMO mm:ss]** for: pricing/licensing view; StormForge optimization in‑UI; commitment purchase & risk profiles; anomaly + budget threshold alerts; modeling/what‑if demo; K8s allocation across EKS/AKS; scheduling + storage optimization.
    
- If helpful, I can also generate a **side‑by‑side “quote → fix” cheat sheet** for the reviewers using the exact snippets above.