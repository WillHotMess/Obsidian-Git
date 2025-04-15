# StormForge Trial User Journey & Nurture Architecture

## Process Overview & Implementation Plan

### 1. User Journey Overview

#### Initial Engagement

- **Sign-up**: User registers for StormForge free trial
	- **Welcome Email**: Immediate HubSpot email with installation instructions and security FAQ

#### Bifurcated Path Based on Installation Status

- **Path A**: User does not install (HubSpot nurture)    
    - **Reminder Email 1 (Day 2):** Installation instructions and video
    - **Reminder Email 2 (Day 5):** Additional prompting with support options
    - **Reminder Email 3 (Day 20):** Still looking for Kubernetes optimization
	    - If no engagement: Added to CloudBolt general nurture OR Business Development Rep

- **Path B**: User installs (HubSpot nurture)
    - **Preliminary Recommendations Email (Day 1):** Initial platform orientation
    - **Complete Recommendations Email (Day 7):** Prompt to review finalized recommendations
    - **GitOps Integration Email (Day 14):** Technical integration instructions
    - **Final Engagement Email (Day 28):** Additional platform value and conversion prompting

#### Conversion Opportunities (Throughout Journey)
- **Option 1**: AWS Pay-Go self-service
- **Option 2**: MQL/Sales engagement (demo request, sales conversation)
- **Timing**: Conversion can occur at any point post-installation

### 2. Technical Requirements

#### Data Integration
- Connect Segment to HubSpot for real-time user action tracking
- Configure event flagging for both sign-up and installation events
- Ensure proper data flow between platforms

#### List Management
- **List A**: Sign-up users (not yet installed)
- **List B**: Installed users (completed installation)
- Automated list management and user segmentation

#### Automation Design
- Configure HubSpot workflows to:
    - Immediately transition users from Path A to Path B upon installation
    - Suppress remainder of non-install nurture once installation occurs
    - Trigger appropriate emails based on user journey stage

#### Content Development
- All email templates staged in HubSpot
- CE templates for personalized outreach
- Clear CTAs for AWS Pay-Go and sales conversation options

#### Reporting
- Create Salesforce reports for 6Sense Conversational Email (CE) campaigns
- Track conversion rates at each journey stage
- Monitor path transitions (non-installed to installed)

### 3. Implementation Timeline

|Phase|Deliverable|Owner|Timeline|
|---|---|---|---|
|1|Segment-to-HubSpot connection|Nick|Week of 4/15|
|2|HubSpot list creation|Marketing Ops|Week of 4/22|
|3|Email templates finalized|Content Team|Week of 4/22|
|4|Automation workflow design|Marketing Ops|Week of 4/29|
|5|Salesforce reports for CE|Sales Ops|Week of 4/29|
|6|Testing & QA|Cross-functional|Week of 5/6|
|7|Go-live|All|Week of 5/13|

### 4. Success Metrics
- **Primary KPIs**:
    - Increase in installation rate (Sign-up to Install conversion)
    - Growth in AWS Pay-Go conversions
    - Increase in qualified sales opportunities
    - Reduction in non-engaged trial users
- **Secondary Metrics**:
    - Email engagement rates
    - Time-to-installation
    - Time-to-first-recommendation application
    - User progression through journey stages

### 5. Next Steps
1. Finalize and approve email content
2. Complete technical integration between Segment and HubSpot
3. Build automation workflows in HubSpot
4. Create reporting dashboards
5. Establish regular review cadence for optimization