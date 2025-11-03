WorkJam NotesWorkJam is a Montreal-based SaaS company operating primarily on Google Cloud Platform with a substantial GKE environment and DynamoDB infrastructure. They're currently spending ~$3 million annually on GKE alone.  
Saurabh: SRE and FinOps Lead ([LinkedIn](https://www.linkedin.com/in/saurabhvichare22/))  

## Opportunity
- Long term there appears to be a product-led opportunity where WorkJam could help guide CloudBolt's development roadmap. Many of their requirements aren't available out-of-the-box from any vendor, presenting a collaborative development opportunity.
- For now, we should try and win on the clear distinction we have in Kubernetes management and GCP cost allocation/reporting, inclusive of effective costs.

## Current State
- Comprehensive cloud infrastructure reporting beyond just GKE
- Currently using KubeCost but actively seeking a non-IBM replacement
- Are evaluating FinOut and Vantage as an alternative

  

## Primary Objectives
- Cloud infrastructure reporting and dashboards beyond just GKE (KubeCost)
- Synthetic tagging capabilities
- Understanding of MSRP vs. Contracted vs. Effective vs. Billed costs
- Cost views that distinguish EDP, CUD, and CUD Flex considerations
- Shared cost allocation across "CompanyID" as the main organizational structure
- Derived unit costs by Company ID, feature, and other dimensions
- Kubernetes Optimization options
- Manually managing pod-node configurations in Excel (clear inefficiency)

## **Advanced Use Cases**
- Seasonality analysis - clear roller coaster patterns in GKE scaling
- ROI calculations for specific features per customer ("Feature X" for "Customer Y")
- Building internal ChatBot features requiring cost attribution
- Network traffic attribution with tracing capabilities
- Integration with existing observability stack (HoneyComb & OpenTelemetry)
- CFO specifically interested in AI functionality - impressed by CloudBolt's patent portfolio

## Procurement
- GCP Procurement preferred with potential private offer arrangement

## Recommended Next Steps
- POC scoping call with deeper technical dive
- Find Easy + Early Wins before diving into more advanced needs (telemetry integration)
- Roadmap mapping session covering short-, medium-, and long-term capabilities