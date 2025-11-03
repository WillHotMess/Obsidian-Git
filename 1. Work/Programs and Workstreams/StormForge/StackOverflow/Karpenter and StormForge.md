

Karpenter + StormForge
Combining Intelligent Cluster and Pod Autoscaling for Peak Efficiency and Reliability

Get a Free Consultation
Intelligent Cluster Autoscaling Reduces Infrastructure Costs
Improper Pod Requests Contribute a Majority of the Waste
Autonomously Manage Resources With Machine Learning
How Karpenter and StormForge are Better Together
Harnessing all three autoscaling dimensions in Kubernetes is essential to achieving efficiency and maximizing cloud ROI, but organizations of all sizes struggle to get it right.

There are native Kubernetes solutions for each of the three types of autoscaling: Cluster Autoscaler (CA), Vertical Pod Autoscaler (VPA), and Horizontal Pod Autoscaler (HPA). Each of these tools presents a different level of complexity that makes achieving proficiency in all three extremely challenging. Misconfigurations often result in uncontrolled costs and risks to application reliability.


The three dimensions of Kubernetes Autoscaling
With organizations caught in a tug-of-war between rising cloud costs and ensuring application reliability, business stakeholders, software developers and platform engineers are often at odds, leading to stalemates.

Achieving efficient autoscaling in Kubernetes requires new capabilities, built on analytics and automation, which can help ease the burden on people, and achieve both cost efficiency and application reliability.

Intelligent Cluster Autoscaling Reduces Infrastructure Costs #
Karpenter is an open-source flexible, high-performance Kubernetes cluster autoscaler that was introduced by AWS in 2021 and donated to the Cloud Native Computing Foundation (CNCF) in 2023. Karpenter is designed to work with any Kubernetes environment, including cloud and on-premises distributions.

Karpenter analyzes the resource request values of unschedulable pods, determines the least-cost compute instances to meet application requirements, and quickly provisions the optimal instance type to run them.

Over time, those instances can become underutilized as some workloads scale down or are removed from the cluster. Karpenter can automatically look for opportunities to reschedule these workloads onto a set of more cost-efficient EC2 instances, whether they are already in the cluster or need to be provisioned.

Organizations can achieve significant infrastructure cost savings by implementing Karpenter and replacing the Kubernetes native Cluster Autoscaler.


Karpenter simplifies Kubernetes infrastructure with the right nodes at the right time. (Image credit: AWS)
📚 Resource Recommendations

Learn more about Karpenter's components, architecture, and practical use cases with these technical guides:

EKS Karpenter: Deep Dive
AKS Karpenter: Deep Dive
Karpenter Consolidation
Karpenter vs Cluster Autoscaler
Improper Pod Requests Contribute a Majority of the Waste #
Karpenter drastically simplifies the configuration of cluster autoscaling and can improve application availability and cluster efficiency to reduce cloud costs. However, Karpenter is not designed to address the more granular need for pod rightsizing, nor does it provide the ability to add and remove pods in response to bursty workloads. 

According to a survey by the CNCF, 49% say Kubernetes has driven cloud spend up, and 70% say workload overprovisioning is the source of overspending. This improper workload resource management results in wasted resources that directly correspond to excessive cloud costs while leaving application performance and availability risks unaddressed.

Solving for these suboptimal pod requests can be challenging as developers and platform engineers spar over what these values should be, how often they should be updated, and ultimately, whose responsibility it is to perform what quickly becomes an excessive amount of manual toil. Kubernetes native solutions like the VPA are insufficient for solving these problems accurately at scale.

Autonomously Manage Resources With Machine Learning #
StormForge Optimize Live rightsizes pods automatically, using machine learning to analyze usage data from workloads to recommend the most efficient CPU and memory settings without risking performance or reliability. Recommendations can be automatically implemented to keep pods continuously rightsized as usage fluctuates.

In addition, StormForge works with the HPA to scale bi-dimensionally, recommending the optimal target utilization to ensure the HPA’s scaling behavior is consistent as the vertical size of the pods change. Because StormForge is managing both the vertical scaling and the HPA target utilization configuration, vertical and horizontal pod autoscaling work synergistically — eliminating thrashing and maximizing pod-level efficiency.

How Karpenter and StormForge are Better Together #
Karpenter is a great solution on its own, but it doesn't keep pods rightsized or scale them in the most efficient way. Using Karpenter alongside StormForge ensures efficient bin packing, i.e. the most streamlined placement of pods on optimally sized nodes, which results in additional cloud cost savings.


By deploying Karpenter and StormForge together, you can maximize efficiency — automatically and intelligently. 

By using Karpenter with StormForge, you can:

Reduce Kubernetes-related cloud costs and resource usage by 50% or more.
Ensure application performance and reliability for higher productivity and a positive customer experience
Free up operational bandwidth from Kubernetes management to focus on innovation and other strategic activities
Experience these benefits yourself with a free 60-minute analysis of how your organization can best utilize Karpenter. 

Signup for the Karpenter Best Practices Service on AWS Marketplace.
 

Latest Resources
Podcast Emergin Kubernetes Blogs copy 20
Video

Emerging Kubernetes tools for AI and optimizing GPU workloads

an illustration of a person fist bumping a robot with an icon for Amazon EKS Auto Mode between them
Video

How to deploy the StormForge agent on EKS Auto Mode

An illustration showing how StormForge rightsizes Kubernetes pod while Amazon EKS Auto Mode ensures efficient bin packing for cloud cost savings
Solution Brief

Amazon EKS Auto Mode

Seeing is Believing
Start getting resizing recommendations minutes from now.

Start A Trial
Enter Sandbox
Watch An Install

Free trial includes full version on 1 cluster for 30 days!

Footer logo cncf member silver color
Footer logo fin ops foundation member
Footer logo aicpa soc
The Gartner Cool Vendor 2023 badge
Footer logo aws marketplace
Product
Resources
Resource Library
Blog
Documentation
Events & Webinars
Company
Careers
Contact Us
News
Partners
Pricing
Start A Trial
Enter Sandbox
© 2025 StormForge | Terms & Conditions | Privacy Policy