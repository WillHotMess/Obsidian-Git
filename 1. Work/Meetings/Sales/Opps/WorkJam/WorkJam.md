
## Meeting Summary: WorkJam Initial Prospect Inquiry

## Company Overview

**WorkJam** is a Montreal-based SaaS company operating primarily on Google Cloud Platform with a substantial GKE environment and DynamoDB infrastructure. They're currently spending **$2-3 million annually on GKE** alone.

## Current State
- Currently using **KubeCost** but actively seeking a non-IBM replacement
- Are evaluating **FinOut** and **vantage** as an alternative
- Manually managing pod-node configurations in Excel (clear inefficiency)

## Primary Objectives
- **Comprehensive cloud infrastructure reporting** beyond just GKE
- **Shared cost allocation across "CompanyID"** as the main organizational structure
- Integration with existing observability stack (**HoneyComb & OpenTelemetry**)
- **Network traffic attribution** with distributed tracing capabilities

## Needs
- **Seasonality analysis** - critical business requirement (clear roller coaster patterns in GKE scaling)
- **ROI calculations** for specific features per customer ("Feature X" for "Customer Y")
- **Derived unit costs** by Company ID, feature, and other dimensions
- Complex cost view requirements including **EDP, CUD, and CUD Flex considerations**

## CFO Notes
- **CFO specifically interested in AI functionality** - impressed by CloudBolt's patent portfolio
- Building internal **ChatBot features** requiring cost attribution

## Technical Integration Points
- **OpenTelemetry and HoneyComb** integration 
- **Synthetic tagging** capabilities needed
- Understanding of **MSRP vs. Contracted vs. Effective vs. Billed costs**

## Procurement
- **GCP Procurement preferred** with potential private offer arrangement

## Opportunity
Long term there appears to be a **product-led POC opportunity** where WorkJam could help guide CloudBolt's development roadmap. Many of their requirements aren't available out-of-the-box from any vendor, presenting a collaborative development opportunity. 
For now, we should try and win on the clear distinction we have in Kubernetes management and GCP cost allocation/reporting, inclusive of effective costs. 

## Recommended Next Steps
1. **POC scoping call** with deeper technical dive
2. Find **Easy + Early Wins** before diving head first into more advanced needs (telemetry integration)
3. **Roadmap mapping session** covering short-, medium-, and long-term capabilities