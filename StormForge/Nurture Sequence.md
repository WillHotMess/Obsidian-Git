# StormForged Product-Led Growth Process Overview

## Contact-to-Customer Journey Flow

| Stage            | Touchpoint            | Timing                 | Channel              | Content/Action                                                                              | Owner       |
| ---------------- | --------------------- | ---------------------- | -------------------- | ------------------------------------------------------------------------------------------- | ----------- |
| **Contact/Lead** | Initial Acquisition   | -                      | Various Sources      | • Contact us form<br>• Event leads<br>• Known contacts<br>• Trial signup                    | Marketing   |
|                  | Signup Confirmation   | Immediate              | HubSpot              | • Thank you email<br>• Installation instructions                                            | Automated   |
|                  | Signup Follow-up      | 48 hours post-signup   | HubSpot              | • Reminder email<br>• "5 mins away from seeing the impact"<br>• Installation video          | Automated   |
|                  | Non-Install Follow-up | Day 7                  | Conversational Email | • "Why didn't you install?"<br>• Offer assistance                                           | Caleb       |
|                  | Continued Outreach    | Day 30                 | Conversational Email | • Follow-up on non-installation<br>• Re-engagement attempt                                  | Caleb       |
|                  | Final Outreach        | Day 45                 | Conversational Email | • Last attempt to engage<br>• Value proposition reminder                                    | Caleb       |
| **MQL**          | Post-Install          | Immediate              | HubSpot              | • Welcome<br>• StoryLane video<br>• Recommendation overview                                 | Automated   |
|                  | Learning Phase        | Post 7 days of install | HubSpot              | • How to install applier<br>• Enroll workloads into auto deploy<br>• Configuration guidance | Automated   |
|                  | Engagement Phase      | 14 days post-install   | HubSpot              | • Evaluating success<br>• Best practices<br>• Advanced features                             | Automated   |
|                  | Advanced Usage        | 21 days                | HubSpot              | • Hook features<br>• Integration possibilities<br>• Success stories                         | Automated   |
|                  | Trial Expiration      | End of trial           | Conversational Email | • Extend trial<br>• Talk to sales rep<br>• Pay-as-you-go option                             | Caleb/Sales |
| **Opportunity**  | Demo Request          | Any time               | -                    | • Demo scheduling<br>• Personalized outreach                                                | Caleb       |

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
