# Lobster × CloudBolt: An Engaging Customer-Led Story

Below is a fully structured narrative you can hand to Ludwig. It shifts the tone from a formavl “TED-talk” to an interactive, customer-driven story that keeps the spotlight on his real-world experience. The outline is timed for a 20–25-minute slot (including a quick live demo) and maps cleanly to 4-5 slides—so Ludwig can own the delivery while CloudBolt supplies supportive visuals.

---

## 1. Welcome & Context (1 min)

**Slide 1 – “Who We Are”**

- 1-sentence intro from the CloudBolt host, then pass the mic.
- Ludwig introduces himself (Platform Engineer, Lobster) and Lobster’s mission: _“Connecting people and data with a no-code iPaaS.”_

_Talking tip:_ Keep this tight—audience came for the story, not corporate bios.

---

## 2. Hybrid Deployment Reality (4 min)

**Slide 2 – “Before CloudBolt: Two Painful Worlds”**

Ludwig walks the audience through on-premise to AWS journey.

1. **Legacy Data Center**
    - 4–6 h manual build → VM template → SSH → hand-edited configs
    - 500 + servers managed by 5 people = constant fire-drills
    - Long checklists, inconsistent ports, security headaches
2. **Home-grown AWS “Click-to-Data” Platform**
    - Looked modern (Lambda, DynamoDB) but 100k+ undocumented Python lines
    - Single-person knowledge silo—unmaintainable when that engineer left
    - Fastish deploys (25–35 min) but existential business risk

---

## 3. Choosing a “Goldilocks” Platform (3 min)

**Slide 3 – “Why CloudBolt Won”**

Ludwig explains the shortlist:

| Evaluated                   | Deal-Breaker                                  |
| --------------------------- | --------------------------------------------- |
| Red Hat Automation Platform | 200-page setup guide, 7 servers just to start |
| Cloudify                    | YAML-only, hard-to-extend                     |
| Morpheus                    | Ubuntu-centric; Lobster is RHEL/Amazon Linux  |
| Status Quo                  | High risk to Customer Delivery                |

**What stood out about CloudBolt**

- “Lego-pieces” approach—reuse Ansible/Terraform/Python skills
- Fast time-to-value: prototype in days, production in <60 days
- No vendor lock-in: if CloudBolt vanished, the IaC still runs

---

## 4. The Transformation (5 min)

**Slide 4 – “After CloudBolt: Quantifiable Impact”**

|Metric|Before|After|
|---|---|---|
|Provisioning time|4–6 h|20–30 min|
|Monthly jobs|N/A|30,000 +|
|Success rate|N/A|99.7%|
|Staff required|5 engineers for 500 servers|**Same team, 10× scale**|

Key points Ludwig highlights:

- Consistent “golden” blueprints eliminate port mix-ups & checklist errors.
- Built-in power-scheduling saved AWS RDS costs by pausing beyond 7-day stop limit.
- Platform now used by Sales Ops, Academy, Support—_“From hammer to Swiss-army knife.”_

---

## 5. Live Moment (5 min)

**Quick Demo – “Order to Credentials in <30 min”**

Ludwig launches a minimal customer environment: fill custom form → submit → show job tracker starting. While it runs, he clicks into:

- Incident-management tab he built in **1 hour** (PagerDuty + OTRS feed).
- Power-schedule hook for RDS.

He returns to show progress ~50% to prove real-time execution.

---

## 6. Unanticipated Wins (3 min)

**Slide 5 – “What We Didn’t Expect”**

- Platform engineering: teams are treated as _internal customers_.
    
- Anyone contributes at their skill level—custom forms, webhooks, or full Python plugins.
    
- Quote collage (German originals + English captions) from Sales, Support, Academy:
    
    “CloudBolt jobs failing <1%—and when they do, it’s usually our typo, not the platform.”
    

---

## 7. Closing & Q &A (3–4 min)

**One-slide visual only—“Key Takeaways”**

1. Speed: 10× faster provisioning.
2. Reliability: 99%+ success at 30k jobs/month.
3. Flexibility: Same tool powers five internal teams.

Hand back to CloudBolt host for audience questions.

---

## Usage Notes for Ludwig

1. **Own the narrative.** Use CloudBolt branding on supporting slides, but keep Lobster’s voice front-and-center.
2. **Lean on anecdotes.** The “three engineers, three duplicate tickets” story is gold—humanizes the metrics.
3. **Keep the demo light.** Focus on _result_, not every button click.
4. **Have one fallback screenshot** in case Wi-Fi misbehaves.

---

## Appendix: Slide Starter Kit (titles & suggested visuals)

1. Who We Are – logo strip + Ludwig headshot
2. Two Painful Worlds – side-by-side cartoon or simple icons
3. Why CloudBolt Won – comparison table
4. Quantifiable Impact – bar/number callouts
5. Unexpected Evolution – quote bubbles

CloudBolt marketing can supply background design; Ludwig drops in text, metrics, and screenshots.