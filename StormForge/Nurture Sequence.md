# StormForged Product-Led Growth Process Overview

## Contact-to-Customer Journey Flow

| Stage            | Touchpoint            | Timing                 | Channel              | Content/Action                                                                              |
| ---------------- | --------------------- | ---------------------- | -------------------- | ------------------------------------------------------------------------------------------- |
| **Contact/Lead** | Initial Acquisition   | -                      | Various Sources      | • Contact us form<br>• Event leads<br>• Known contacts<br>• Trial signup                    |
|                  | Signup Confirmation   | Immediate              | HubSpot              | • Thank you email<br>• Installation instructions                                            |
|                  | Signup Follow-up      | 48 hours post-signup   | HubSpot              | • Reminder email<br>• "5 mins away from seeing the impact"<br>• Installation video          |
|                  | Non-Install Follow-up | Day 7                  | Conversational Email | • "Why didn't you install?"<br>• Offer assistance                                           |
|                  | Continued Outreach    | Day 30                 | Conversational Email | • Follow-up on non-installation<br>• Re-engagement attempt                                  |
|                  | Final Outreach        | Day 45                 | Conversational Email | • Last attempt to engage<br>• Value proposition reminder                                    |
| **MQL**          | Post-Install          | Immediate              | HubSpot              | • Welcome<br>• StoryLane video<br>• Recommendation overview                                 |
|                  | Learning Phase        | Post 7 days of install | HubSpot              | • How to install applier<br>• Enroll workloads into auto deploy<br>• Configuration guidance |
|                  | Engagement Phase      | 14 days post-install   | HubSpot              | • Evaluating success<br>• Best practices<br>• Advanced features                             |
|                  | Advanced Usage        | 21 days                | HubSpot              | • Hook features<br>• Integration possibilities<br>• Success stories                         |
|                  | Trial Expiration      | End of trial           | Conversational Email | • Extend trial<br>• Talk to sales rep<br>• Pay-as-you-go option                             |
| **Opportunity**  | Demo Request          | Any time               | -                    | • Demo scheduling<br>• Personalized outreach                                                |

## Supporting Educational Content

|Content Type|Topics|Purpose|
|---|---|---|
|How-to Videos|• Product overview<br>• Installation<br>• Configuration<br>• Recommendation application|Reduce friction in trial journey|
|StoryLane Guides|• Interactive walkthroughs<br>• Step-by-step processes<br>• UI familiarization|Visual learning and engagement|
|Documentation|• Using SF with Argo<br>• Karpenter integration<br>• Configuration maps<br>• Best practices|Technical enablement|

## Technical Dependencies

|Requirement|Timeline|Owner|Status|
|---|---|---|---|
|Segment to HubSpot connection|Week of 4/15|Nick|Planned|
|Nurture email review|-|William|Pending|
|Email automation setup|Post-Segment integration|-|Pending|
|Content creation prioritization|-|Team|Pending|


Sign-up -> 
Install (Yes/No) -> 
Pursued Engagement (via Intercom, AWS Pay-Go, CE, sales outreach, or other mechanism) (Yes/No)
End of the sequence (put into CloudBolt nurture)

```
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#1976D2', 'primaryTextColor': '#000', 'primaryBorderColor': '#0D47A1', 'lineColor': '#333', 'secondaryColor': '#2E7D32', 'tertiaryColor': '#D32F2F' }}}%%

  

flowchart TD

    %% Main journey flow

    A([User Signs Up]) -->|Day 0| B["Welcome Email

    Subject: Getting Started with Your StormForge free trial

    • Installation instructions

    • Security FAQ

    • Sandbox environment option"]

    B --> C{User Installed?}

    %% No Install Path with email content

    C -->|No| D["Reminder Email 1 (Day 2)

    Subject: Reminder: Install a cluster to start rightsizing

    • 15-second installation video

    • Benefits overview"]

    D --> E{User Installed?}

    E -->|No| F["Reminder Email 2 (Day 5)

    Subject: Reminder about your StormForge trial

    • Installation instructions

    • Support options"]

    F --> G{User Installed?}

    G -->|No| H["Sales: Personalized Outreach (Day 7)"]

    H --> I{User Responded?}

    I -->|No| J["Sales: Follow-up (Day 30)"]

    J --> K{User Responded?}

    K -->|No| L["Sales: Final Outreach (Day 45)"]

    L --> M{User Engaged?}

    M -->|No| N[Add to CloudBolt General Nurture]

    %% Yes Install Path with email content

    C -->|Yes| O["Preliminary Recommendations Email

    Subject: Your preliminary recommendations are ready

    • Login instructions

    • Review preliminary recommendations

    • Support contact"]

    O --> P["Complete Recommendations Email (Day 7 post-install)

    Subject: Your rightsizing recommendations are ready to apply

    • Review financial impact

    • Apply recommendations

    • Technical support options"]

    P --> Q["GitOps Integration Email (Day 14 post-install)

    Subject: Deploying recommendations with GitOps

    • GitOps integration information

    • Application methods"]

    Q --> R{Recommendations

    Applied?}

    R -->|Yes| S["Trial Ending - Recommendations Applied Email

    Subject: Your trial ends soon, how's it going?

    • Account upgrade information

    • Pricing contact"]

    R -->|No| T["Trial Ending - Recommendations Not Applied Email

    Subject: Your trial ends soon, do you need more time?

    • Extension options

    • Technical support contact"]

    S --> U{Trial Expired}

    T --> U

    %% Trial Expiration Options

    U --> V{User Action?}

    V -->|Extend Trial| W[Trial Extended +15 days]

    W --> R

    V -->|Talk to Sales| X[Create Opportunity & Route to Sales]

    V -->|Pay-As-You-Go| Y[Self-Service AWS Marketplace]

    V -->|No Action| N

    %% User Engagement Paths from No Install

    E -->|Yes| O

    G -->|Yes| O

    I -->|Yes| Z{Engagement Type}

    K -->|Yes| Z

    M -->|Yes| Z

    %% Engagement Types

    Z -->|Product Question| AA[Direct to Product Team]

    Z -->|Sales Interest| X

    Z -->|Technical Help| BB[Schedule Technical Support Call]

    %% Demo Request Can Happen Anytime

    CC([Demo Request]) --> X

    %% Intercom Engagement Can Happen Anytime

    DD([Intercom Message]) --> Z

    %% Styling

    classDef default fill:#ffffff,stroke:#333,stroke-width:1px

    classDef email fill:#BBDEFB,stroke:#1565C0,stroke-width:2px

    classDef action fill:#C8E6C9,stroke:#2E7D32,stroke-width:2px

    classDef negative fill:#FFCDD2,stroke:#C62828,stroke-width:2px

    classDef outreach fill:#FFE0B2,stroke:#E65100,stroke-width:2px

    classDef decision fill:#FFF9C4,stroke:#F57F17,stroke-width:2px

    classDef entry fill:#D1C4E9,stroke:#4527A0,stroke-width:2px

    class A,CC,DD entry

    class B,D,F,O,P,Q,S,T email

    class H,J,L outreach

    class N negative

    class W,X,Y,AA,BB action

    class C,E,G,I,K,M,R,U,V,Z decision
```