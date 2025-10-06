keyword: kubernetes rightsizing

slug: /solutions/kubernetes-rightsizing

HTML title: Autonomous Kubernetes Rightsizing | CloudBolt

Meta Description: Rightsize Kubernetes workloads in real time with ML-powered insights. CloudBolt slashes costs, prevents OOMKills, and optimizes JVM workloads.

---

# Kubernetes Rightsizing Hero Page

**Eyebrow:** Kubernetes Rightsizing

# Continuous Kubernetes Rightsizing Engineers Can Trust

Cut costs, eliminate performance risks, and scale optimization across clusters with a platform purpose-built for complex Kubernetes environments.

[Start Free StarTrial](https://app.stormforge.io/signup/) [Enter Sandbox](https://app.stormforge.io/sandbox/)

---

## Trusted by platform teams managing thousands of workloads

[Customer logos placeholder]

---

# Purpose-built for the reality of production Kubernetes

**Eyebrow:** Eliminate Manual Toil

## No More Manual Tuning for CPU and Memory Requests

Your developers shouldn’t have to guess, and your platform team shouldn’t burn cycles tweaking YAML. Our ML-powered engine analyzes usage patterns every 15 seconds to forecast demand and rightsize resources automatically—adjusting in real-time to daily usage spikes and long-term trends.

[See it in action](https://app.stormforge.io/sandbox/)

**Eyebrow:** PERFORMANCE WITHOUT COMPROMISE

## Rightsizing That Works With Your Autoscalers

Unlike basic tools that break HPA, our bi-dimensional scaling harmonizes vertical and horizontal pod adjustments. We fine-tune both resource requests and HPA utilization targets—cutting overprovisioning while avoiding CPU throttling, latency issues, or OOMKills.

[See it in action](https://stormforge.io/videos/getting-started-optimize-live-install/)

**Eyebrow:** JVM WORKLOADS

## The Only Rightsizer That Understands Java

Standard rightsizing tools miss the mark with Java. We go deeper—optimizing JVM heap sizes and container memory limits in tandem, so your memory footprint shrinks without triggering GC storms or container crashes.

[See it in action](https://app.stormforge.io/signup/)

**Eyebrow:** Enterprise Scale

## Built to Optimize Thousands of Workloads, Automatically

Deployed across some of the largest Kubernetes estates in the world. We auto-discover every pod, learn its patterns in days, and apply optimization recommendations within policy-defined guardrails. Integrates directly into your GitOps pipelines—no rewrites required.

[See it in action](https://app.stormforge.io/signup/)

---

# Feature Highlights

**ML-Forecasting:** Proactively predict resource needs by analyzing seasonal trends and HPA behavior instead of just reacting to past usage.

**Bi-dimensional Scaling:** Harmonize vertical and horizontal pod scaling to work in concert, preventing them from conflicting during workload adjustments.

**JVM Optimization:** Collect deep metrics to fine-tune both Java heap sizes and container limits, eliminating OOMKills and excessive garbage collection.

**Policy Automation:** Automatically discover workloads, learn usage patterns, and apply recommendations safely within configurable, policy-driven guardrails.

**GitOps Integration:** Deploy recommendations as patches or manifests directly through your existing CI/CD pipelines and workflows.

**Enterprise Visibility:** Gain a unified view of optimization opportunities and realized savings across all of your clusters, namespaces, and workloads.

---

## Why Platform Engineers Choose CloudBolt

**✓ 90% faster time-to-savings** From months to hours, for immediate cost reductions.

**✓ Reduced manual work** Eliminate repetitive, unsustainable resource tuning.

**✓ 40-60% Kubernetes savings** Right-size workloads and reduce your node footprint.

**✓ 99% allocation accuracy** Maximize node efficiency and avoid wasted spend.

---

# What our customers say

“StormForge has added immediate gains by overall net-capacity savings due to overprovisioned workloads.” - Mark Piersak, US Bank Vice President, Manager, Container Platform Solutions

“StormForge was easy for me to get up and running quickly, and we achieved immediate efficiencies that reduced our cloud costs and lowered the amount of toil we had from manually configuring requests.” - Ulf Mansson, Realforce Sr. Principal Cloud Architect

“The machine learning that StormForge leverages to set requests and limits on pods allows our engineering and SRE teams to focus on our customer experience rather than infrastructure settings.” - Ed Brennan, Acquia Chief Software Architect

---

# Frequently asked questions

**Is StormForge delivered as a SaaS solution or available for on-premises deployment?**

StormForge Optimize Live uses a hybrid architecture. The StormForge Agent runs entirely within your Kubernetes cluster (on-premises), collecting metrics and applying recommendations locally. The web application and machine learning control plane are SaaS-hosted, accessible at [app.stormforge.io](http://app.stormforge.io). This gives you the security of keeping your workload data within your environment while providing the convenience of a managed service for analysis and recommendations.

**How is StormForge hosted within Kubernetes environments?**

The StormForge Agent is deployed as a Helm chart directly into your Kubernetes cluster in the stormforge-system namespace. It runs alongside your applications, collecting metrics every 15 seconds and applying recommendations locally. The SaaS control plane processes the machine learning analysis and provides the web interface for viewing recommendations and configuring optimization settings. No application data leaves your cluster - only anonymized usage metrics are transmitted.

**How can recommendations from StormForge be applied?**

You have complete flexibility in how you apply recommendations. During the initial 7-day learning period, you can only apply recommendations manually for review. After that, you can: 1) Apply recommendations on-demand through the web UI with "Apply Now", 2) Enable automatic deployment by setting the live.stormforge.io/auto-deploy annotation to "Enabled" for hands-free optimization, or 3) Integrate recommendations into your CI/CD workflow by downloading patches from the UI or using the StormForge CLI. You can also configure deployment thresholds to ensure only impactful changes trigger pod restarts.

**What is the difference between autoscaling and rightsizing, and how does StormForge support both?**

Yes, StormForge provides bi-dimensional autoscaling that combines both approaches. **Horizontal autoscaling** (like HPA) adds or removes pod replicas in seconds to handle traffic spikes, while **vertical rightsizing** continuously optimizes the CPU and memory requests and limits for each container over hours, days, and weeks. Unlike basic VPA tools that conflict with HPA, StormForge uses forecast-based machine learning to harmonize both dimensions. We optimize the resource settings of the pods that sit on your nodes (requests/limits), while tools like Karpenter optimize the nodes themselves. This gives you the best of both worlds - rapid scaling for performance and intelligent rightsizing for cost efficiency.

---

# Ready to put Kubernetes rightsizing on autopilot?

Start reducing your Kubernetes costs _without_ sacrificing performance. See it work with your actual workloads—risk-free.

[Start Free Trial](https://app.stormforge.io/signup/) [Enter Sandbox](https://app.stormforge.io/sandbox/)

_Free trial includes full optimization on 1 cluster for 30 days._

---

## Resources for Kubernetes Platform Teams

**[Solution guide]** StormForge is now part of CloudBolt [https://www.cloudbolt.io/solution-guides/stormforge-is-now-part-of-cloudbolt/](https://www.cloudbolt.io/solution-guides/stormforge-is-now-part-of-cloudbolt/)

**[Blog]** Introducing Pay-as-You-Go Pricing on AWS Marketplace [https://stormforge.io/blog/introducing-pay-as-you-go-pricing-on-aws-marketplace/](https://stormforge.io/blog/introducing-pay-as-you-go-pricing-on-aws-marketplace/)

**[Blog]** How to Use StormForge Optimize Live’s Java Workload Optimization [https://stormforge.io/blog/how-to-use-stormforge-optimize-lives-java-workload-optimization/](https://stormforge.io/blog/how-to-use-stormforge-optimize-lives-java-workload-optimization/)

**[eGuide]** Kubernetes Pod Scheduling: Tutorial and Best Practices [https://www.cloudbolt.io/kubernetes-pod-scheduling/](https://www.cloudbolt.io/kubernetes-pod-scheduling/)