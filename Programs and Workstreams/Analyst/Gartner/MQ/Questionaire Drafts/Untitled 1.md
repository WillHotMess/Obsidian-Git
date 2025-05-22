Does your CFM offering support the execution of recommended actions from within your solution?

The CloudBolt platform supports comprehensive execution of recommended actions directly within our solution across all major cloud environments and service types. Our integrated approach enables organizations to move seamlessly from cost optimization insights to immediate action implementation without requiring external tools or manual intervention across IaaS, Kubernetes, and SaaS environments.

CloudBolt delivers native action execution capabilities through three integrated modules that address the complete spectrum of cloud financial management:

**1. Multi-Cloud Infrastructure Optimization**: Our core platform executes recommended actions across all major public and private cloud environments including AWS, Azure, GCP, OCI, VMware, and Azure VMware Solution (AVS). Users can implement cost-saving measures directly through the CloudBolt interface, including resource right-sizing, termination, scheduling adjustments, and commitment management optimizations.

**2. Kubernetes Workload Optimization**: Through our integrated Kubernetes module, CloudBolt enables direct execution of Kubernetes optimization recommendations regardless of where clusters are hosted. The platform applies machine learning-driven resource recommendations directly to Kubernetes workloads, automatically adjusting CPU and memory allocations, HPA configurations, and other container resource settings to optimize both cost and performance.

**3. SaaS License Management**: Our Saas module provides automated execution capabilities for SaaS and licensing optimization. The platform analyzes usage patterns to identify unused or underutilized licenses and implements automated license harvesting and reclamation workflows that reclaim, reallocate, downgrade, or cancel licenses to eliminate unnecessary spend while ensuring only active users occupy paid seats.

## Customer Use Cases

A global technology company leveraged CloudBolt's comprehensive action execution capabilities across their hybrid cloud environment. They implemented automated right-sizing for their AWS and Azure infrastructure workloads, resulting in 28% cost reduction on compute resources. Simultaneously, their Kubernetes clusters running on both public cloud and on-premises VMware infrastructure benefit from StormForge's automated optimization, achieving an additional 35% efficiency improvement in container resource utilization. The integrated SaaS management through CloudEagle identified and reclaimed over 200 unused software licenses across their organization, generating $150,000 in annual savings.

A financial services firm uses CloudBolt's multi-cloud execution engine to implement consistent optimization policies across their AWS primary environment and OCI disaster recovery infrastructure. The platform automatically executes scheduling policies for development environments, implements automated backup lifecycle management, and optimizes reserved instance utilization across both cloud providers through unified policy management.

## Technical Details

CloudBolt's action execution framework operates through a unified orchestration engine that maintains consistent policy management and audit trails across all modules. The platform utilizes direct API integration with cloud providers, Kubernetes clusters, and SaaS platforms to implement recommendations without intermediate tools or manual processes. Our execution engine supports various implementation modes including immediate execution, scheduled deployment, and approval-based workflows, all managed through a single interface that provides complete visibility into optimization actions across the entire technology stack.

---

Does your CFM offering support automating the execution of recommended actions? (Answer YES only if the automation engine is natively built into your solution.) 

Yes, CloudBolt's Cloud Financial Management platform supports comprehensive automation of recommended action execution through our natively built automation engine. Our Cloud Native Actions framework transforms manual FinOps processes into continuous, automated optimization workflows that execute cost-saving actions without human intervention, reducing insight-to-action time from weeks or months to minutes or hours.

CloudBolt's native automation engine delivers sophisticated policy-driven execution across all cloud environments through four core automation capabilities:

**1. Continuous Policy-Based Automation**: Our Cloud Native Actions framework enables organizations to create custom intelligent policies that automatically execute optimization recommendations based on configurable waste signals and business rules. The automation engine continuously monitors resource utilization patterns and implements cost-saving actions according to predefined policies without requiring manual intervention.

**2. Intelligent Waste Signal Automation**: CloudBolt's automation engine leverages configurable waste signals that detect idle, underutilized, or inefficient resources across all cloud environments. When waste signals fire and meet policy criteria, the system automatically implements appropriate remediation actions including resource right-sizing, termination, scheduling changes, or tagging for lifecycle management.

**3. Multi-Cloud Automated Optimization**: The platform's native automation capabilities extend across AWS, Azure, GCP, OCI, VMware, and hybrid environments, enabling consistent automated optimization policies regardless of cloud provider. Organizations can implement automated right-sizing, commitment management, and resource lifecycle policies that execute seamlessly across their entire multi-cloud infrastructure.

**4. Kubernetes Automated Right-Sizing**: Through our integrated StormForge module, CloudBolt provides machine learning-driven automated optimization for Kubernetes workloads. The system continuously analyzes container resource usage patterns and automatically applies optimized CPU and memory configurations, HPA adjustments, and other container resource modifications to maintain optimal cost-performance balance.

CloudBolt's automation engine operates through a distributed architecture that processes waste signals, evaluates policy conditions, and executes optimization actions through direct cloud provider APIs. The system maintains complete audit trails of all automated actions, supports rollback capabilities for critical resources, and provides configurable safety controls including resource exclusion rules, execution time windows, and approval gates for high-impact changes. The automation framework integrates natively with existing DevOps CI/CD pipelines through webhook APIs and supports custom automation workflows through our extensible policy language.



---


Does your CFM offering support the implementation of scheduled actions on target cloud resources? (Scheduled actions may include tasks such as turning virtual machines on or off and adjusting the storage performance tier.)

Yes, CloudBolt's CFM platform supports comprehensive implementation of scheduled actions on target cloud resources across all major cloud environments. CloudBolt enables organizations to automate time-based resource management operations including virtual machine start/stop scheduling, storage tier adjustments, and other lifecycle management tasks that optimize costs while maintaining operational requirements.
- **Resource Lifecycle Automation**: Beyond basic start/stop operations, CloudBolt automates storage tier adjustments, backup scheduling, snapshot management, and resource tagging for lifecycle policies that align with organizational cost optimization requirements.
- **Orchestration Module Lifecycle Management**: Our Orchestration module provides expiration policies for automated tear down and decommissioning of resources based on configurable timeframes. This ensures temporary resources, development environments, and project-based infrastructure are automatically cleaned up to prevent cost accumulation.
- **Custom Autoscaling Policies**: CloudBolt supports scheduled resizing policies that enable custom autoscaling beyond standard cloud provider capabilities. Organizations can implement sophisticated scaling schedules based on business patterns, seasonal demands, or operational requirements.
- **Custom Webhook Integration**: CloudBolt provides custom webhook action options that allow users to set policies triggering automated actions to any external software or system, enabling integration with proprietary tools and specialized automation systems.

--- 


Does your CFM offering support automatically stopping resources by detecting their idle/unused state using external metrics? (This capability involves automatically identifying when a system is idle by monitoring external metrics like network traffic or load balancer activity. For instance, if a virtual machine shows no network traffic over a certain period, it is likely unused and can be stopped. Unlike scheduling, this functionality does not rely on internal metrics such as CPU or memory usage, nor does it require the user to set up a scheduling window.) 


Yes, CloudBolt's CFM platform supports automatically stopping resources by detecting idle/unused states using external metrics through our Cloud Native Actions framework. Our configurable waste signals monitor monitor performance activity to identify truly idle resources that should be terminated, moving beyond traditional CPU/memory-based detection to provide more accurate idle resource identification.

CloudBolt's external metrics-based idle detection delivers intelligent resource management through:

**1. Configurable External Waste Signals**: Our Cloud Native Actions framework enables creation of waste signals that monitor external metrics including network traffic levels, load balancer activity, and other external indicators to identify idle resources. These signals can be tuned to detect resources with minimal external activity over configurable time periods.

**2. Advanced Idle Detection Logic**: Unlike traditional approaches that rely solely on internal CPU or memory metrics, CloudBolt analyzes external connectivity patterns and traffic flows to determine if resources are genuinely unused. A virtual machine showing no network traffic over a specified period triggers idle detection regardless of internal resource utilization.

**3. Multi-Cloud External Monitoring**: The platform integrates with cloud provider monitoring services and external observability tools to gather network traffic data, load balancer metrics, and other external indicators across AWS, Azure, GCP, OCI, and hybrid environments.

**4. Policy-Driven Automation**: When external metrics indicate idle state based on configured thresholds, CloudBolt automatically executes termination policies without manual intervention. Organizations can customize detection criteria based on environment type, resource tags, and business requirements.

**5. Custom Webhook Integration**: External metrics detection can trigger custom webhook actions to integrate with specialized monitoring systems or external automation platforms beyond standard cloud provider capabilities.

--- 

Does your CFM offering manage the workflow for remediation actions? (A remediation workflow oversees the progression of cost-related actions, coordinating among multiple stakeholders through the stages of detection, notification, validation, execution, or dismissal of a budget violation or optimization opportunity. Answer YES only if your solution handles this workflow natively, without relying on third-party integrations.)

Does your CFM offering integrate with workflow management systems to manage the remediation workflow? (Answer YES only if you offer this integration out-of-the-box, without the need for customers to write code or use your API. Integrations that are only possible through your SDK or API do not qualify for this question. Common external workflow management systems used for this purpose include ServiceNow and Jira Software.)



--- 

CloudBolt maintains dedicated vertical-specific sales resources with our most significant investment focused on the federal government sector. Our federal team represents a comprehensive, specialized approach that goes beyond traditional sales coverage to deliver sector-specific expertise and localized support.

**Federal Government Specialization**
Our federal vertical team is strategically based in the Washington D.C. area and includes dedicated account managers, specialized engineers, and customer success professionals who work directly on-site with government agencies and federal partners. This team understands the unique compliance requirements, procurement processes, and operational challenges specific to federal environments, including FedRAMP certification requirements, security protocols, and government-specific cloud adoption patterns.

**Dedicated Investment Structure**
The federal vertical receives its own dedicated budget allocation covering marketing initiatives, channel development programs, and specialized sales efforts. This investment structure enables CloudBolt to develop government-specific messaging, participate in federal industry events, maintain necessary security clearances, and build partnerships with federal system integrators and resellers. The dedicated budget ensures our federal team can respond quickly to RFP opportunities and maintain the specialized certifications required for government business.

**Localized Expertise and Support**
Our D.C.-area presence enables direct, on-site engagement with federal customers, which is often critical for government procurement cycles and ongoing relationship management. The team's proximity to key decision-makers and their understanding of federal budget cycles, procurement timelines, and compliance requirements provides significant advantages in serving this complex vertical market.

