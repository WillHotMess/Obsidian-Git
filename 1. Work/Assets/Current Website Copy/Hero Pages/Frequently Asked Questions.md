keyword: N/A

slug: /faq

HTML title: Frequently Asked Questions | CloudBolt

Meta Description: Get clear answers to your cloud management FAQs. Learn how CloudBolt helps with FinOps, automation, billing, integrations, and multi-cloud governance.

---

## FinOps

**Which clouds does CloudBolt support?**

Our FOCUS-native architecture provides comprehensive multi-cloud support across AWS, Azure, GCP, and Oracle Cloud Infrastructure, plus deep integration with private cloud environments including VMware, Nutanix, and OpenStack through our CloudBolt agent.

**What cost allocation and billing flexibility does CloudBolt provide?**

CloudBolt delivers sophisticated cost allocation with granular re-rating capabilities, custom markup application, and flexible allocation rules that can be applied at multiple organizational levels.

For service providers and resellers, we offer native multi-tenant architecture with customer-scoped portals, automated invoice generation, commitment pooling, and full white-labeling capabilities to support complex billing scenarios and margin management.

**What optimization and automation features are included in CloudBolt?**

Our platform combines AI/ML-powered cost optimization with automated remediation through our Cloud Native Actions framework. This includes anomaly detection, rightsizing recommendations across IaaS and containers (enhanced by our StormForge acquisition), idle resource detection, and policy-driven automation that can execute optimizations automatically or through configurable approval workflows.

**What integrations and workflow capabilities does CloudBolt offer?**

CloudBolt provides out-of-the-box, bi-directional integrations with ServiceNow, Jira, Slack, and Microsoft Teams, enabling seamless workflow management from cost detection through remediation. Our comprehensive RESTful API and extensive integration ecosystem allow for custom workflows, automated ticketing, and notifications that fit into existing operational processes.

---

## Cloud Management

**Does CloudBolt support multiple clouds and hypervisors?**

Yes, CloudBolt provides comprehensive support for hybrid and multi-cloud environments with over 25 out-of-the-box integrations. This includes all major public clouds (AWS, Azure, GCP, Oracle Cloud, IBM Cloud), private cloud platforms (VMware vSphere, Hyper-V, Nutanix, OpenStack, Red Hat OpenShift), and container orchestration platforms (Kubernetes, OpenShift). Our platform serves as a unified control plane across your entire technology portfolio, enabling consistent management regardless of the underlying infrastructure.

**Does CloudBolt provide self-service portals and automated resource provisioning?**

CloudBolt delivers a modern, intuitive self-service portal that simplifies cloud consumption for end users while maintaining IT governance and control. The platform includes extensive automation capabilities with advanced orchestration logic, enabling you to create streamlined workflows that eliminate manual effort and reduce operational overhead. Users can request and provision resources through standardized service catalogs while IT maintains oversight through built-in approval processes and policy enforcement.

**What integrations does CloudBolt offer with existing tools?**

CloudBolt provides unmatched integration capabilities that connect with virtually any technology offering programmatic access. This includes out-of-the-box support for ServiceNow and other ITSM platforms, Infrastructure as Code tools like Terraform and Ansible, identity management systems (Active Directory, SAML2 providers like Azure Entra ID and Okta), security platforms (Splunk, SIEM solutions), and backup solutions (Veeam, Cohesity, Rubrik). Our Python-based extensible architecture ensures you can integrate with any system in your environment without disrupting existing investments.

**Does CloudBolt enable granular access controls and governance policies?**

Yes, CloudBolt includes comprehensive governance capabilities with role-based access control (RBAC), granular permission settings, and customizable approval workflows. The platform enforces least-privilege access principles while enabling you to define conditional policies through our built-in Rules Engine. You can implement governance controls at every stage of the resource lifecycle, from provisioning through day-2 operations, ensuring consistent policy enforcement across all environments while maintaining audit trails for compliance requirements.

**Does CloudBolt include cost management and FinOps capabilities?**

CloudBolt's suite includes robust FinOps capabilities that provide real-time visibility into cloud spending across all environments through unified dashboards and detailed cost breakdowns. The platform implements cost governance policies including approval thresholds, budget controls, and quota enforcement, while AI-powered analytics identify unusual spending patterns and optimization opportunities. Features include predictive cost forecasting, intelligent workload placement recommendations, and automated optimization workflows that help balance innovation with cost efficiency across your hybrid cloud environment.

---

## Kubernetes Optimization

**Is StormForge delivered as a SaaS solution or available for on-premises deployment?**

StormForge Optimize Live uses a hybrid architecture. The StormForge Agent runs entirely within your Kubernetes cluster (on-premises), collecting metrics and applying recommendations locally. The web application and machine learning control plane are SaaS-hosted, accessible at [app.stormforge.io](http://app.stormforge.io). This gives you the security of keeping your workload data within your environment while providing the convenience of a managed service for analysis and recommendations.

**How is StormForge hosted within Kubernetes environments?**

The StormForge Agent is deployed as a Helm chart directly into your Kubernetes cluster in the stormforge-system namespace. It runs alongside your applications, collecting metrics every 15 seconds and applying recommendations locally. The SaaS control plane processes the machine learning analysis and provides the web interface for viewing recommendations and configuring optimization settings. No application data leaves your cluster - only anonymized usage metrics are transmitted.

**How can recommendations from StormForge be applied?**

You have complete flexibility in how you apply recommendations. During the initial 7-day learning period, you can only apply recommendations manually for review. After that, you can: 1) Apply recommendations on-demand through the web UI with "Apply Now", 2) Enable automatic deployment by setting the live.stormforge.io/auto-deploy annotation to "Enabled" for hands-free optimization, or 3) Integrate recommendations into your CI/CD workflow by downloading patches from the UI or using the StormForge CLI. You can also configure deployment thresholds to ensure only impactful changes trigger pod restarts.

**What is the difference between autoscaling and rightsizing, and how does StormForge support both?**

Yes, StormForge provides bi-dimensional autoscaling that combines both approaches. **Horizontal autoscaling** (like HPA) adds or removes pod replicas in seconds to handle traffic spikes, while **vertical rightsizing** continuously optimizes the CPU and memory requests and limits for each container over hours, days, and weeks. Unlike basic VPA tools that conflict with HPA, StormForge uses forecast-based machine learning to harmonize both dimensions. We optimize the resource settings of the pods that sit on your nodes (requests/limits), while tools like Karpenter optimize the nodes themselves. This gives you the best of both worlds - rapid scaling for performance and intelligent rightsizing for cost efficiency.