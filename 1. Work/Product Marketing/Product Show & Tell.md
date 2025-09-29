# Product & Engineering Weekly Meeting Recap

## Meeting Details
- **Title**: Product & Engineering Weekly Demo Session
- **Date**: September 26, 2025
- **Meeting Type**: Internal Product Demo & Review

## Summary
The team presented 12 major feature demonstrations across CloudBolt Platform, CMP, and Stormforge products. Key highlights included significant customer-requested features (Azure onboarding automation, RISP sharing for Rapid Scale), AI/ML innovations (MCP integration for CMP, MLOps monitoring), and infrastructure improvements (Kubernetes cost allocation, multi-tenant authentication). Several features are production-ready while others are in final testing phases.

---

## Feature Analysis

### 1. Custom Form Errors Enhancement (CMP)
**What was demoed:**
- Improved error handling for custom forms in CMP, displaying blueprint validation errors and server-tier errors at the top of the screen
- Users can now fix errors directly in the form
- Quota submission errors are now properly captured and displayed
- Preview mode now shows validation errors

**Why it's important:**
- Custom forms allow flexible metadata collection during resource provisioning
- Previously, error mapping between custom UI and backend was problematic
- Improves user experience by making errors clear and actionable

**How it helps customers:**
- Reduces frustration when provisioning resources
- Allows customers to fix errors without leaving the form
- Better validation feedback prevents failed deployments
- Maintains flexibility of custom forms while improving usability

**When ready to ship:**
- **Already shipped** - Feature is complete and in production

---

### 2. Operating System Dependencies (CMP)

**What was demoed:**
- New capability to create dependencies based on specific operating systems (not just OS family)
- Dynamic field visibility based on OS selection (e.g., RHEL 8 vs RHEL 9 shows different satellite server fields)
- Generated options can now reference specific OS versions
- Example: Different fields appear for Windows vs Linux, and even RHEL 8 vs RHEL 9

**Why it's important:**
- Customers have requested this for "quite a long time"
- Different OS versions often require different configuration options (encryption, disk backends, flavors)
- Previously required custom code workarounds

**How it helps customers:**
- Enables OS-specific configuration options automatically
- Reduces manual scripting for OS-dependent workflows
- Makes blueprints more intelligent and context-aware
- Supports complex scenarios like Azure Gen 2 VMs with specific encryption requirements

**When ready to ship:**
- **Already shipped** - Feature is complete and available

---

### 3. Kubernetes Cost Allocation

**What was demoed:**
- Stormforge agent now collects per-container, per-pod metrics (usage, requests, limits)
- Data flows from Stormforge clusters → AMP → S3 → Snowflake
- New data pipeline using Snowpipe for real-time ingestion
- DBT models for data transformation in Snowflake (replacing AWS Athena)
- Data updates every 30 minutes

**Why it's important:**
- Enables accurate Kubernetes cost tracking at container/pod level
- Provides foundation for showing cost impact over time
- Critical for DirectTV and Pega use cases
- Aligns Stormforge costs with actual billing data

**How it helps customers:**
- Accurate cost allocation for Kubernetes workloads
- Better visibility into where costs are occurring
- Foundation for showing savings over time
- Enables chargeback/showback models

**When ready to ship:**
- **In progress** - Data pipeline working as of demo (September 26), still being refined for production readiness. Not yet ready for customer rollout.

---

### 4. Multi-Tenant Authentication (Stormforge)

**What was demoed:**
- Auth0-based organization support allowing users to belong to multiple tenants
- Organization chooser UI when logging in
- Ability to switch between organizations without re-authentication
- Admin panel updates for managing multi-tenant memberships
- Simplified customer SSO setup (customers can configure IDPs themselves)

**Why it's important:**
- Previously users could only belong to one tenant
- Essential for CloudBolt's tenant/subtenant model
- Reduces support burden for SSO configuration
- Foundation for RBAC improvements

**How it helps customers:**
- Support staff and MSPs can access multiple customer tenants easily
- Customers can self-configure SSO/IDP without CloudBolt involvement
- Better matches CloudBolt CMP's existing tenant structure
- Simplifies multi-customer management for MSPs

**When ready to ship:**
- **Available in dev environment** - Moving to stage next week (week of October 2), production rollout timing TBD

---

### 5. Recommendation Validity Period (Stormforge)

**What was demoed:**
- Separation of recommendation schedule from validity period
- New `--valid-for` flag (e.g., P1D for 1 day, P14D for 14 days)
- CLI-based demonstration showing different recommendations based on validity period
- Different recommendations produced for 1-day vs 14-day validity on same workload

**Why it's important:**
- HSBC requested this "a long time ago"
- Critical for customers not using auto-deploy (Trumid, WeChat TV/Mulesoft, HSBC)
- Addresses gap between recommendation generation and manual application
- Enables daily recommendations with longer validity periods

**How it helps customers:**
- HSBC: Generate daily updates for showback but allow developers to apply recommendations that last weeks
- Trumid: CLI-driven workflows with appropriate validity windows
- WeChat TV: Mulesoft clusters with manual approval processes need longer validity
- Prevents recommendations from becoming stale before application

**When ready to ship:**
- **API implemented** - Currently CLI-only, UI work in progress. Not yet production-ready for customer-facing use.

---

### 6. Azure Onboarding Automation Script

**What was demoed:**
- Comprehensive Azure CLI-based onboarding script
- Automated setup for: billing account integration, FOCUS export creation, role assignments, storage account creation
- Interactive session with logging and configuration management
- Supports both CSMP and new platform in single installation
- Secret rotation capability
- Creates downloadable configuration file for session persistence

**Why it's important:**
- Azure onboarding documentation is "very disjointed" and complex
- Customers struggle with manual role assignments and permissions
- Reduces onboarding from hours to minutes
- Peter reported "nothing but good things" from AWS version

**How it helps customers:**
- Non-technical users can onboard without Azure expertise
- Eliminates manual configuration errors
- Significantly reduces time to value
- Single script works for both CSMP and new platform
- Clear permission requirements documented upfront

**When ready to ship:**
- **Production ready** - Script complete and tested, documentation being finalized. AWS version already successful with customers.

---

### 7. New UI Testing Migration (Platform)

**What was demoed:**
- Converted ~30 E2E tests to work with new React UI
- Tests run every 30 minutes against staging
- Playwright-based test for cost reports shown
- Tests verify GraphQL responses against UI table data
- Handles multiple filter combinations and metrics

**Why it's important:**
- Provides confidence for UI changes
- Catches regressions automatically
- Validates data accuracy between API and UI
- Critical for new platform reliability

**How it helps customers:**
- Ensures stable, bug-free experience
- Faster feature delivery with confidence
- Reduced production issues

**When ready to ship:**
- **In PR review** - Tests updated and ready, awaiting merge to run against new UI continuously

---

### 8. AI-Powered CMP Interaction (MCP)

**What was demoed:**
- MCP (Model Context Protocol) server enabling natural language interaction with CMP API
- Voice/chat-based blueprint deployment
- Examples: "Show me available blueprints", "What are my most popular blueprints", "Deploy grist server"
- Assembles deployment payloads through conversational interface
- Live demonstration in Cursor IDE

**Why it's important:**
- Leidos specifically requested this capability 3-4 weeks ago
- Aligns with enterprise trend toward agentic interfaces
- Differentiates CloudBolt through ease of use
- Enables voice-driven provisioning workflows

**How it helps customers:**
- Dramatically simplifies self-service provisioning
- Reduces training requirements for end users
- Enables voice-based workflows for specific verticals
- Makes complex catalog navigation intuitive
- Future: Wrapping Terraform scripts for simplified execution

**When ready to ship:**
- **Early demo stage** - Working proof of concept, needs refinement. Rick estimates "weeks" not months. Planning to demo to Leidos soon.

---

### 9. React UI Improvements (Platform)

**What was demoed:**
- **Feature Flags with Flagsmith**: Runtime feature toggling without code deploys, tenant-specific feature control
- **Collapsible Navigation**: Toggle sidebar for more screen space, preference persists across sessions, tooltips for collapsed icons

**Why it's important:**
- Feature flags enable controlled rollouts and quick bug response
- Previously required developer + code deploy for flag changes
- Collapsible nav provides more screen real estate
- Both were highly requested by users

**How it helps customers:**
- Feature flags: Safer feature releases, customer-specific enablement, instant rollback capability
- Collapsible nav: Better UX, more space for dashboards and reports
- Marketing and support can control features without engineering

**When ready to ship:**
- **Already deployed** - Both features live in production

---

### 10. RISP Sharing for Rapid Scale

**What was demoed:**
- Re-rating engine that backs out AWS RI/SP discounts to list price
- 45 Rapid Scale customer tenants onboarded with RISP rules
- Data scoping from master payer to individual customer organizations
- UI showing build cost vs adjusted build cost
- Automated tenant provisioning from customer account lists

**Why it's important:**
- Rapid Scale is grandfathered into AWS RI/SP sharing program
- Enables MSPs to show accurate costs to sub-customers
- Critical for Rapid Scale's business model
- Foundation for other MSP re-rating needs

**How it helps customers:**
- MSPs can properly allocate RI/SP benefits to customers
- Customers see list price, MSP adds credit line items separately
- Supports Rapid Scale's discount program presentation
- Foundation for automated RI/SP re-application for other customers

**When ready to ship:**
- **Nearly production ready** - Working in dev, final fix being promoted. Nick meeting with Rapid Scale on Tuesday (October 2) to potentially demo.

---

### 11. Applier Change Management Workflow (Stormforge)

**What was demoed:**
- Webhook integration for Stormforge applier sending change notifications
- JSON payload to customer-specified endpoints
- Reference architecture: API Gateway → Lambda → SNS → multiple subscribers (Slack, JIRA, SQS, S3)
- Demonstration of live patch with notifications to Slack and SQS
- Long-term storage in S3 for audit trail

**Why it's important:**
- Pega specifically requested this capability
- Applier makes direct changes to clusters - customers need audit trail
- Enables integration with enterprise change management workflows
- Provides historical record of all changes

**How it helps customers:**
- Audit compliance for cluster changes
- Integration with existing ITSM workflows
- Alerts for every change Stormforge makes
- Long-term retention for analysis (beyond current logs)
- Enables automated approvals and ticketing

**When ready to ship:**
- **Production ready** - Feature implemented in applier, documentation complete, delivered to Pega who reported being "very happy about it"

---

### 12. MLOps Monitoring & Analysis (Stormforge)

**What was demoed:**
- Analysis of 162,000 workloads across 7 customers
- Breakdown of optimization impact by workload size and category
- Key finding: Microservices optimized well (reducing resources), large workloads see resource increases
- Discovery: Large workloads (5% of total) consume 54% of cluster resources
- Insight: Many recommendations don't change over time, indicating optimization opportunity

**Why it's important:**
- First systematic visibility into live worker performance at scale
- Identifies optimization strategy improvements by workload type
- Reveals significant COGS reduction opportunities
- Validates product claims about steady-state optimization
- Addresses customer requests for value demonstration (Pega, DirectTV)

**How it helps customers:**
- Foundation for "value realization" reporting customers need
- Data for CFO-level ROI discussions
- Potential for quarterly industry trend reports (like DataDog)
- Enables workload-specific optimization strategies
- Answers "what are you actually saving me?" questions

**When ready to ship:**
- **Analysis/monitoring tool** - This is internal tooling for product improvement, not a customer-facing feature. However, the insights will inform customer-facing reports. Timeline for customer-facing value reporting: TBD, requires additional data capture (actual applications, not just recommendations).

---

## Key Themes & Takeaways

1. **Customer-Driven Development**: Multiple features directly responding to specific customer requests (RISP sharing for Rapid Scale, MCP for Leidos, change management for Pega, validity period for HSBC)
2. **AI/ML Integration**: Two significant AI initiatives (MCP for CMP, MLOps monitoring) positioning CloudBolt as modern and innovative
3. **MSP Enablement**: Strong focus on multi-tenant capabilities and re-rating for MSPs (Rapid Scale, multi-org auth)
4. **Operational Excellence**: Infrastructure improvements (Kubernetes cost allocation, feature flags, automated onboarding) reducing friction
5. **Value Demonstration Gap**: Clear acknowledgment that showing realized savings remains a challenge; MLOps analysis is first step toward solution

## Action Items
- [ ] Nick to demo RISP sharing to Rapid Scale on Tuesday, October 2 (pending final fix)
- [ ] Schedule demo of MCP integration for Leidos (Rick, Mike, Nick)
- [ ] Create recorded demos for external use of key CMP features (Stephen, Mike Rombert, Will)
- [ ] Add Pega to MLOps analysis dataset (Ryan, Reed)
- [ ] Finalize Azure onboarding script documentation (CP, Peter)
- [ ] Move multi-tenant auth to stage environment (Stefan - week of October 2)
- [ ] Continue UI work for recommendation validity period (team TBD)
- [ ] Complete GCP onboarding script (CP)
- [ ] Consider Data Dog-style quarterly trend reports using MLOps data (Ryan, marketing)

## Follow-up
- Next meeting: October (specific date not mentioned)
- Noted need for internal meetings on CMP UI refresh progress (Yasmin, Auggie, Ly)
- Marketing to work with Rick on MCP demo recording when ready (Mark, Will)