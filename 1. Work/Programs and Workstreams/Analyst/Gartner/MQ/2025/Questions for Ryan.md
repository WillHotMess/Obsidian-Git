# Forecasting, Anomaly Detection & Workload Optimization Questions

## Forecasting & Cost Estimation Questions

**Q4** - Does your CFM offering provide cost modeling capabilities that enable users to model workloads and estimate costs based on user-defined characteristics and consumption forecasts?
- *Examples of user inputs include CPU, memory, storage, cluster configurations, and expected network throughput*

**Q5** - Does your CFM offering provide cloud-agnostic cost models that allow users to generate cost estimates for deploying workloads to multiple cloud providers?

**Q6** - Does your CFM offering enable customers to perform simulated "what if" analysis on existing workloads to assess the impact of potential changes to their current cloud configuration?
- *Answer YES only if customers can manually select alternative resource types/size for their existing workloads and assess the cost impact*

**Q7** - Does your CFM offering have the capability to estimate the cost of infrastructure-as-code (IaC) models prior to deployment?

**Q8** - Does your CFM offering support cloud migration planning by discovering a source environment and using the discovered data to predict future cloud costs if the environment is migrated to a target cloud provider?

**Q23** - Does your CFM offering provide capabilities to forecast future cloud costs based on historical data?

**Q38** - Does your CFM offering trigger alerts when projected end-of-period spending is forecasted to exceed the defined budget?

## Anomaly Detection Questions

**Q39** - Does your CFM offering trigger alerts on detected cost anomalies?
- *Answer YES only if your solution can detect cost anomalies like unexpected, abnormal cost spikes or sudden changes in cost trends that may require immediate attention*

## Core Workload Optimization Questions

### Resource Right-Sizing & Configuration
**Q41** - Does your CFM offering provide rightsizing recommendations?
- *Focuses on changing configuration parameters related to service type or size, including virtual machines, containers or serverless*

**Q42** - Does your CFM offering detect and report on idle/unused resources?

**Q43** - Does your CFM offering provide scheduling recommendations?
- *Pertains to detecting intermittent utilization patterns and recommend a scheduling window*

### Service-Specific Optimization
**Q44** - Does your CFM offering provide storage services optimization?

**Q45** - Does your CFM offering provide container services optimization?
- *Answer YES only if your solution includes specific optimization features tailored for cloud-based container services*

**Q46** - Does your CFM offering provide data and analytics services optimization?

**Q47** - Does your CFM offering provide AI services optimization?

**Q48** - Does your CFM offering provide optimization for other serverless services beyond what you have already described in the previous questions?
- *Example: adjustment of allocated memory for serverless functions*

### Advanced Optimization Recommendations
**Q49** - Does your CFM offering provide recommendations to optimize in-guest software installed in containers or virtual machines?
- *Answer YES only if your capability specifically optimizes software solutions (e.g., Apache Spark or Databricks) that are installed in-guest*

**Q50** - Does your CFM offering provide recommendations to change architectural patterns or components to more cost-effective alternatives?
- *Such as transitioning application components to managed services or serverless versions*

**Q51** - Does your CFM offering provide recommendations for optimizing application code to enhance resource efficiency and lower performance requirements?

**Q52** - Does your CFM offering provide recommendations to implement horizontal autoscaling?
- *Answer YES only if your capability can generate recommendations based on observed application characteristics*

**Q53** - Does your CFM offering provide recommendations to migrate standard virtual machines to preemptible (or "spot") machines?
- *Based on observed application characteristics such as statelessness or ability to interrupt the workload*

## Optimization Analysis & Risk Management

**Q54** - Does your CFM offering provide a risk analysis related to the execution of recommended optimization actions?

**Q55** - Does your CFM offering provide a ROI analysis related to the execution of recommended optimization actions?
- *Should offer estimate of effort needed to implement and track return of implemented actions*

**Q56** - Does your CFM offering aggregate and list cost optimization recommendations from sources that are external to your CFM offering?
- *Recommendations from other CFM solutions or native recommendations provided by cloud service providers*

## Commitment & Purchase Optimization

**Q57** - Does your CFM offering provide recommendations to purchase programmatic commitments based on observed utilization patterns?
- *AWS Reserved Instances, Azure Savings Plans and Google Committed Use Discounts*

**Q58** - Does your CFM offering provide recommendations for changing the scope of purchased commitments to enhance their coverage and utilization?

**Q59** - Does your CFM offering provide capabilities to manage risk according to user preference to inform commitment recommendations?
- *Ability to define a risk profile that informs commitment recommendations*

## Automation & Execution Questions

### Manual Execution Support
**Q68** - Does your CFM offering support the execution of recommended actions from within your solution?
- *Answer YES only if the remediation can be initiated from within your UI or API*

### Automated Optimization
**Q69** - Does your CFM offering support automating the execution of recommended actions?
- *Answer YES only if the automation engine is natively built into your solution*

**Q70** - Does your CFM offering support the implementation of scheduled actions on target cloud resources?
- *Scheduled actions may include turning virtual machines on or off and adjusting storage performance tier*

**Q71** - Does your CFM offering support automatically stopping resources by detecting their idle/unused state using external metrics?
- *Automatically identifying when a system is idle by monitoring external metrics like network traffic*

**Q72** - Does your CFM offering support autoscaling of container clusters to optimize for cost and performance?

**Q76** - Does your CFM offering support the automatic migration of workloads between standard and preemptible (or "spot") machines to optimize for cost and availability?

### Commitment Automation
**Q61** - Does your CFM offering provide capabilities to purchase commitments or change their scope of applicability through automation?
- *Answer YES only if your capability can use automation to execute commitment actions to maximize discount while minimizing risk*

## Supporting Optimization Questions

**Q75** - Does your CFM offering gather user feedback on the quality of cost-related alerts and recommendations to minimize false positives?

**Q79** - Does your CFM offering monitor the potential savings of identified cost optimization opportunities?

**Q80** - Does your CFM offering monitor the savings generated from optimization recommendations that have been successfully implemented or automated?

## Summary by Category:

**Forecasting & Estimation**: 7 questions (Q4-8, Q23, Q38)
**Anomaly Detection**: 1 question (Q39)
**Core Workload Optimization**: 13 questions (Q41-53)
**Optimization Analysis**: 3 questions (Q54-56)
**Commitment Optimization**: 3 questions (Q57-59, Q61)
**Automation & Execution**: 6 questions (Q68-72, Q76)
**Supporting Functions**: 3 questions (Q75, Q79-80)

