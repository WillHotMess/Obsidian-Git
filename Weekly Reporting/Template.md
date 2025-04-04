# Weekly Sales Pipeline Analysis Project - Claude Implementation Guide

## Project Overview

Create a Claude-powered automation that performs in-depth analysis of sales pipeline data and generates a comprehensive executive email summarizing key metrics, activity patterns, and opportunities requiring attention. The system should run weekly to track ongoing pipeline health and activity trends across the sales team.

## Data Sources

The primary input is a CSV export from your CRM containing opportunity data with the following key fields:

- Opportunity Source
- Created Fiscal
- Type
- Account Name
- Opportunity Owner
- Opportunity Name
- Annual Recurring Revenue
- Created Date
- Close Date
- Age
- Last Activity Date
- Inactive Days
- Next Steps
- Forecast Category
- Stage

## Key Analyses to Perform

### 1. Pipeline Metrics Analysis

- Track MQLs, SALs, SQLs, and opportunities against budget targets
- Calculate total pipeline value and breakdown by stage
- Compare current quarter performance to targets

### 2. Activity & Engagement Analysis

- Categorize opportunities by activity recency:
    - Recent (0-7 days)
    - Mid (8-14 days)
    - Stale (15+ days)
- Identify opportunities with critical inactivity
- Calculate activity percentages by stage
- Compare actual contact frequency to recommended frequency:
    - Qualification/Discovery: 3-4 contacts/week
    - Prove/Solution Design: 5-7 contacts/week
    - Negotiation: 8-10 contacts/week

### 3. Next Steps Validation

- Parse the "Next Steps" field to extract dates
- Identify discrepancies between CRM activity dates and Next Steps dates
- Flag opportunities where team is logging activity in notes but not updating CRM

### 4. Age vs. Close Date Analysis

- Compare opportunity age to projected close dates
- Calculate projected total sales cycles
- Identify unrealistic close date projections (e.g., >540 days total cycle)
- Analyze sales cycle projections by age bucket and stage

### 5. High-Value/At-Risk Identification

- Create list of top 10 opportunities by ARR
- Highlight both high-performing and at-risk opportunities
- Calculate "concern scores" based on value and inactivity
- Identify specific opportunities requiring intervention

## Email Structure

The weekly email should follow this consistent format:

1. **Introduction**: Brief overview of weekly performance
2. **Pipeline Highlights**: Key metrics with percentage to budget
    - MQLs, SALs, SQLs, Opportunities
    - Pipeline value by stage
    - Total open opportunities
3. **Activity Status Overview**: Table showing activity status by stage
    - Recent/mid/stale percentages
    - ARR by stage
    - Highlight concerning percentages
4. **Top Opportunities Analysis**: Table of top deals with activity details
    - Opportunity name, owner, stage, ARR, inactive days, status
    - Group into "progressing well" vs "requiring intervention"
5. **Key Recommendations**: Strategic actions based on analysis
    - Specific opportunities to focus on
    - Process improvements needed
    - Forecasting adjustments

## Implementation Requirements

### Technical Approach

1. Create a Claude application that:
    
    - Accepts CSV data as input
    - Performs all analyses using Python/pandas
    - Generates formatted email content
    - Flags data quality issues (like date discrepancies)
2. Implement the following analytical functions:
    
    - `calculate_pipeline_metrics(data)`: Track performance vs targets
    - `analyze_activity_patterns(data)`: Calculate activity status by stage
    - `parse_next_steps(data)`: Extract dates from next steps field
    - `compare_age_to_close(data)`: Evaluate close date realism
    - `identify_critical_opportunities(data)`: Flag deals needing attention
3. Implement output formatting:
    
    - Create markdown tables for activity status and top deals
    - Generate email body with proper sections and formatting
    - Include data visualizations if appropriate

### Handling Special Cases

1. Incorporate "notes vs CRM data" validation to catch activity tracking issues
2. Make age vs close date analysis adjustable based on sales cycle assumptions
3. Allow for quarter transition handling (like in the Q1→Q2 transition example)

### Quality Checks

1. Flag potential data issues in the CRM for review
2. Check for unrealistic projections and highlight in the email
3. Identify opportunities that have been in the same stage too long

## Example Email Templates

Reference the examples provided in our discussion for ideal email structure and tone, including:

1. The detailed Q1 pipeline analysis
2. The Q2 week 1 update with low initial numbers but strong existing pipeline

## Implementation Timeline

1. Parse CSV and perform basic metric calculations
2. Implement activity pattern analysis
3. Add next steps parsing and validation
4. Develop age vs close date analysis
5. Create opportunity prioritization logic
6. Build email template generation
7. Implement data quality validation
8. Test with historical data
9. Deploy for weekly execution