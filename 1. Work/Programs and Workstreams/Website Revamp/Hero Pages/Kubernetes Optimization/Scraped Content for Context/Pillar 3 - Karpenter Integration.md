
# Karpenter + StormForge

Combining Intelligent Cluster and Pod Autoscaling for Peak Efficiency and Reliability

[Get a Free Consultation](https://aws.amazon.com/marketplace/pp/prodview-pmfisiuqkxxz6?sr=0-3&ref_=beagle&applicationId=AWSMPContessa)

- [Intelligent Cluster Autoscaling Reduces Infrastructure Costs](https://stormforge.io/solution-brief/karpenter-stormforge/#intelligent-cluster-autoscaling-reduces-infrastructure-costs)
- [Improper Pod Requests Contribute a Majority of the Waste](https://stormforge.io/solution-brief/karpenter-stormforge/#improper-pod-requests-contribute-a-majority-of-the-waste)
- [Autonomously Manage Resources With Machine Learning](https://stormforge.io/solution-brief/karpenter-stormforge/#autonomously-manage-resources-with-machine-learning)
- [How Karpenter and StormForge are Better Together](https://stormforge.io/solution-brief/karpenter-stormforge/#how-karpenter-and-stormforge-are-better-together)

Harnessing all [three autoscaling dimensions](https://stormforge.io/kubernetes-autoscaling/) in Kubernetes is essential to achieving efficiency and maximizing cloud ROI, but organizations of all sizes struggle to get it right.

There are native Kubernetes solutions for each of the three types of autoscaling: [Cluster Autoscaler](https://stormforge.io/kubernetes-autoscaling/kubernetes-cluster-autoscaler/) (CA), [Vertical Pod Autoscaler](https://stormforge.io/kubernetes-autoscaling/vertical-pod-autoscaler/) (VPA), and [Horizontal Pod Autoscaler](https://stormforge.io/kubernetes-autoscaling/horizontal-pod-autoscaler/) (HPA). Each of these tools presents a different level of complexity that makes achieving proficiency in all three extremely challenging. Misconfigurations often result in uncontrolled costs and risks to application reliability.

![](https://stormforge.io/uploads/images/Guides/1-Kubernetes-autoscaling-dimensions.webp)

The three dimensions of Kubernetes Autoscaling

With organizations caught in a tug-of-war between rising cloud costs and ensuring application reliability, business stakeholders, software developers and platform engineers are often at odds, leading to stalemates.

Achieving efficient autoscaling in Kubernetes requires new capabilities, built on analytics and automation, which can help ease the burden on people, and achieve both cost efficiency and application reliability.

## Intelligent Cluster Autoscaling Reduces Infrastructure Costs [#](https://stormforge.io/solution-brief/karpenter-stormforge/#intelligent-cluster-autoscaling-reduces-infrastructure-costs "Direct link to Intelligent Cluster Autoscaling Reduces Infrastructure Costs")

[Karpenter](https://stormforge.io/kubernetes-autoscaling/eks-karpenter/) is an open-source flexible, high-performance Kubernetes cluster autoscaler that was introduced by AWS in 2021 and donated to the Cloud Native Computing Foundation (CNCF) in 2023. Karpenter is designed to work with any Kubernetes environment, including cloud and on-premises distributions.

Karpenter analyzes the resource request values of unschedulable pods, determines the least-cost compute instances to meet application requirements, and quickly provisions the optimal instance type to run them.

Over time, those instances can become underutilized as some workloads scale down or are removed from the cluster. Karpenter can automatically look for opportunities to reschedule these workloads onto a set of more cost-efficient EC2 instances, whether they are already in the cluster or need to be provisioned.

Organizations can achieve [significant infrastructure cost savings](https://aws.amazon.com/solutions/case-studies/picpay-eks-case-study/) by implementing Karpenter and replacing the Kubernetes native Cluster Autoscaler.

![](https://stormforge.io/uploads/images/campaign-landing-pages/Karpenter-overview-on-white.png)

Karpenter simplifies Kubernetes infrastructure with the right nodes at the right time. (Image credit: [AWS](https://karpenter.sh/))

**📚** **Resource Recommendations**

Learn more about Karpenter's components, architecture, and practical use cases with these technical guides:

- [EKS Karpenter: Deep Dive](https://stormforge.io/kubernetes-autoscaling/eks-karpenter/)
- [AKS Karpenter: Deep Dive](https://stormforge.io/kubernetes-autoscaling/aks-karpenter/)
- [Karpenter Consolidation](https://stormforge.io/kubernetes-autoscaling/karpenter-consolidation/)
- [Karpenter vs Cluster Autoscaler](https://stormforge.io/kubernetes-autoscaling/karpenter-vs-cluster-autoscaler/)

## Improper Pod Requests Contribute a Majority of the Waste [#](https://stormforge.io/solution-brief/karpenter-stormforge/#improper-pod-requests-contribute-a-majority-of-the-waste "Direct link to Improper Pod Requests Contribute a Majority of the Waste")

Karpenter drastically simplifies the configuration of cluster autoscaling and can improve application availability and cluster efficiency to reduce cloud costs. However, Karpenter is not designed to address the more granular need for pod rightsizing, nor does it provide the ability to add and remove pods in response to bursty workloads. 

According to a survey by the CNCF, **49% say Kubernetes has driven cloud spend up, and 70% say workload overprovisioning is the source of overspending**. This improper workload resource management results in wasted resources that directly correspond to excessive cloud costs while leaving application performance and availability risks unaddressed.

Solving for these suboptimal pod requests can be challenging as developers and platform engineers spar over what these values should be, how often they should be updated, and ultimately, whose responsibility it is to perform what quickly becomes an excessive amount of manual toil. Kubernetes native solutions like the VPA are insufficient for solving these problems accurately at scale.

## Autonomously Manage Resources With Machine Learning [#](https://stormforge.io/solution-brief/karpenter-stormforge/#autonomously-manage-resources-with-machine-learning "Direct link to Autonomously Manage Resources With Machine Learning")

StormForge [Optimize Live](https://stormforge.io/optimize-live/) rightsizes pods automatically, using machine learning to analyze usage data from workloads to recommend the most efficient CPU and memory settings without risking performance or reliability. Recommendations can be automatically implemented to keep pods continuously rightsized as usage fluctuates.

In addition, StormForge works with the HPA to [scale bi-dimensionally](https://stormforge.io/blog/introducing-intelligent-bi-dimensional-autoscaling/), recommending the optimal target utilization to ensure the HPA’s scaling behavior is consistent as the vertical size of the pods change. Because StormForge is managing both the vertical scaling and the HPA target utilization configuration, vertical and horizontal pod autoscaling work synergistically — eliminating thrashing and maximizing pod-level efficiency.

## How Karpenter and StormForge are Better Together [#](https://stormforge.io/solution-brief/karpenter-stormforge/#how-karpenter-and-stormforge-are-better-together "Direct link to How Karpenter and StormForge are Better Together")

Karpenter is a great solution on its own, but it doesn't keep pods rightsized or scale them in the most efficient way. Using Karpenter alongside StormForge ensures efficient bin packing, i.e. the most streamlined placement of pods on optimally sized nodes, which results in additional cloud cost savings.

![](https://stormforge.io/uploads/images/SF-Karpenter-1.webp)

By deploying Karpenter and StormForge together, you can maximize efficiency — automatically and intelligently. 

By using Karpenter with StormForge, you can:

- Reduce Kubernetes-related cloud costs and resource usage by 50% or more.
- Ensure application performance and reliability for higher productivity and a positive customer experience
- Free up operational bandwidth from Kubernetes management to focus on innovation and other strategic activities

Experience these benefits yourself with a **free 60-minute analysis** of how your organization can best utilize Karpenter. 

[Signup](https://aws.amazon.com/marketplace/pp/prodview-pmfisiuqkxxz6?sr=0-3&ref_=beagle&applicationId=AWSMPContessa) for the Karpenter Best Practices Service on AWS Marketplace.  
 

### Latest Resources

[

![Podcast Emergin Kubernetes Blogs copy 20](https://stormforge.io/uploads/images/preview-images/videos/Podcast-Emergin-KubernetesBlogs-copy-20.png)

Video

Emerging Kubernetes tools for AI and optimizing GPU workloads





](https://stormforge.io/videos/emerging-kubernetes-tools-for-ai-and-optimizing-gpu-workloads/ "Learn More")[

![an illustration of a person fist bumping a robot with an icon for Amazon EKS Auto Mode between them](https://stormforge.io/uploads/images/Blog-Cards/Auto-Mode-Rightsizing-OG.webp)

Video

How to deploy the StormForge agent on EKS Auto Mode





](https://stormforge.io/videos/how-to-deploy-stormforge-agent-eks-auto-mode/ "Learn More")[

![An illustration showing how StormForge rightsizes Kubernetes pod while Amazon EKS Auto Mode ensures efficient bin packing for cloud cost savings](https://stormforge.io/uploads/images/Illustrations/EKS-Auto-Mode-StormForge-greyBG.webp)

Solution Brief

Amazon EKS Auto Mode





](https://stormforge.io/solution-brief/amazon-eks-auto-mode/ "Learn More")

## Seeing is Believing

Start getting resizing recommendations minutes from now.

[Start A Trial](https://app.stormforge.io/logout?signup=true)[Enter Sandbox](https://app.stormforge.io/login/sandbox)

[

Watch An Install

](https://stormforge.io/videos/getting-started-optimize-live-install/)

Free trial includes full version on 1 cluster for 30 days!

![Footer logo cncf member silver color](https://stormforge.io/uploads/images/Logos/footer-logo-cncf-member-silver-color.webp)

![Footer logo fin ops foundation member](https://stormforge.io/uploads/images/Logos/footer-logo-fin-ops-foundation-member.webp)

![Footer logo aicpa soc](https://stormforge.io/uploads/images/Logos/footer-logo-aicpa-soc.webp)

![The Gartner Cool Vendor 2023 badge](https://stormforge.io/uploads/images/Logos/gartner-cool-vendor-2023.webp)

![Footer logo aws marketplace](https://stormforge.io/uploads/images/Logos/footer-logo-aws-marketplace.webp)

[](https://stormforge.io/solution-brief/karpenter-stormforge/#)

- [Product](https://stormforge.io/optimize-live/)

- [Resources](https://stormforge.io/resources/)
- [Resource Library](https://stormforge.io/resources/)
- [Blog](https://stormforge.io/blog/)
- [Documentation](https://docs.stormforge.io/)
- [Events & Webinars](https://stormforge.io/events/)

- [Company](https://stormforge.io/company/)
- [Careers](https://stormforge.io/company/careers/)
- [Contact Us](https://stormforge.io/company/contact-us/)
- [News](https://stormforge.io/company/news/)
- [Partners](https://stormforge.io/company/partners/)

- [Pricing](https://stormforge.io/pricing/)

[Start A Trial](https://app.stormforge.io/logout?signup=true)[Enter Sandbox](https://app.stormforge.io/login/sandbox)

[](https://x.com/StormForgeIO)[](https://github.com/thestormforge)[](https://www.linkedin.com/company/stormforge/)[](https://www.youtube.com/@stormforgeio)

© 2025 StormForge | [Terms & Conditions](https://stormforge.io/terms-and-conditions/) | [Privacy Policy](https://stormforge.io/privacy-policy/)