Q: Does your CFM offering support the normalization of billing data from different cloud providers into a single data model? (Support for the FOCUS specification is not applicable to this question, as it is addressed separately.)

A: Yes, CloudBolt enables users to normalize public, hybrid, and private cloud billing data within a unified model. CloudBolt can seamlessly connect and ingest data across AWS, Azure, GCP, VMware, OCI, OpenStack, Kubernetes, and Nutanix. Users can also connect billing data relating to various SaaS providers for a true single pane of glass covering all IT related costs. 
CloudBolt quickly developed features to support new FOCUS formatted data exports from cloud providers while leveraging existing data collectors to provide users with a seamless experience to centralize all billing data. New and existing users can aggregate, allocate, report, budget, and forecast against costs in a cloud agnostic context. 
Enhance team collaboration by having all stakeholders speak a shared language of cloud costs, utilization, and performance indicators.
Compare apples-to-apples to make smarter multi-cloud decisions around usage optimization, rate negotiations, and more.
Develop highly transferable and valuable FinOps data analysis skillsets that work consistently across any cloud or organizational context.
https://docs.cloudbolt.io/articles/#!cloudbolt-platform-1-0/add-cloud-account-credentials

--- 
Q:

Does your CFM offering provide functionality to normalize tags discovered on deployed resources?
Answer YES only if you provide a normalization layer that can replace tags in billing reports after normalizing them according to some rules aimed at addressing misspelling and other inconsistencies.

A: Yes, CloudBolt enables users to normalize tags across all identified accounts and resources. Customers can create groups that are scoped to 1+ tags to account for inconsistencies in tagging strategy. CloudBolt groups can be named to the normalized version of a tag, or users can implement group tags to associate related identifiers with the group. An example of this is a customer creating normalized tag groups for all application IDs and creating group tags for all that link cost centers, departments, and business units.


--- 
Q: 
Does your CFM offering include a set of baseline cost reports displayed on a dashboard that does not require user configuration?

A: 
Yes

CloudBolt provides a set of pre-configured, out-of-the-box reports that give organizations immediate visibility into their cloud costs and usage patterns. These reports are automatically generated and do not require any additional setup or configuration. This feature is particularly useful for organizations that want to quickly gain insights into their cloud spending without the need for extensive customization or technical expertise.

Baseline reports and dashboard include single and multi-cloud views with filtered versions based on FOCUS service categories.

--- 

Q: 
Does your CFM offering provide functionality to normalize tags discovered on deployed resources?

Answer YES only if you provide a normalization layer that can replace tags in billing reports after normalizing them according to some rules aimed at addressing misspelling and other inconsistencies.

A:
Yes, CloudBolt enables users to normalize tags across all identified accounts and resources. Customers can create groups that are scoped to 1+ tags to account for inconsistencies in tagging strategy. CloudBolt groups can be named to the normalized version of a tag, or users can implement group tags to associate related identifiers with the group. An example of this is a customer creating normalized tag groups for all application IDs and creating group tags for all that link cost centers, departments, and business units.


---

Q: Does your CFM offering support the management of cloud budget approvals before deploying resources in a cloud environment?
Answer YES only if your solution handles the workflow of requesting and receiving approvals to one or more designated budgetholders

A:
Yes, CloudBolt supports the management of cloud spending approvals prior to deploying resources in a cloud environment. Resource deployments can be controlled by various approval workflows based on cloud spend, budgetary, or quota constraints. These constraints can be global or inherited based on the end user and their associated IAM groups. The tool delineates organizational hierarchies, activating approval workflows for resource deployments in both public and private clouds, alongside triggering specific alerts based on groups and services.

CloudBolt's platform includes several key approval workflows:

- Order Submission: Executes when an order is submitted for approval. This is mainly used to integrate CloudBolt with third-party change management systems.
    
- Post-Order Approval: Executes after an order is approved and before jobs are created. This is used to alter job parameters before they are executed.
    
- Post-Order Completion: Executes when an order is marked as completed (either as a success or a failure).
    
- Both the "Order Submission" and "Post-Order Approval" trigger points are used in custom Order Approval workflows, allowing for detailed control over the approval process.