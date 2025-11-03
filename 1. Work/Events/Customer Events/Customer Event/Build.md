
## **SLIDE: Why Self-Service for Build**

### Slide Title: **The $1 Trillion Gap Between Cloud's Promise and Your Reality**

### Main Content:

**Public Cloud won because of self-service.**

- 2006: AWS let developers provision infrastructure in 3 minutes
- 2025: Your developers still wait weeks or months for cloud infrastructure
- Why? 

**The hidden cost of no self-service:**

- **Shadow IT explosion:** [30–40% of enterprise IT spend occurs as shadow IT outside formal governance](<$2.3M average annual spend outside IT governance>)
- **Developer productivity:** 61% cite environment provisioning as a major roadblock in time to production turnaround. [(1)](https://www.businesswire.com/news/home/20230321005525/en/New-Research-Uncovers-a-Developer-Experience-Gap-for-Provisioning-Environments-Resulting-in-Modern-Application-Deployment-Delays)
- **Compliance risk:** 44% of organizations reported a cloud data breach, with misconfigurations/human error the top root cause.[x](https://www.infosecurity-magazine.com/news/cloud-breaches-half-organizations/)

**The uncomfortable truth:** Your teams have two choices today:
1. Wait long cycles for approved infrastructure
2. Swipe a credit card and go rogue

**There's a third way →**

### Speaker Notes (Auggy):

"Let's address the elephant in the room. Every one of you moved to cloud for speed and agility. But here's what I'm seeing at Fortune 500s every week: You've recreated the exact problem cloud was supposed to solve.

One customer told me last month - their Cloud Center of Excellence has 47 approval steps for a production deployment. FORTY-SEVEN. Their developers just started using personal AWS accounts.

The irony? AWS became a trillion-dollar company doing one thing: removing IT as a bottleneck. Not through innovation, not through better security - through self-service. And 20 years later, most enterprises still haven't figured out how to deliver that internally without losing control."

---

## **SLIDE: The Self-Service Myth That's Costing You Millions**

### Slide Title: **Myth: "Self-Service is All or Nothing"**

### Visual: Split screen showing two extremes with a spectrum below

**The False Binary:**

❌ **"Lock Everything Down"**
- Month long deployment cycles from code-to-production
- 61% cite environment provisioning as the Major Roadblock [(1)](https://www.businesswire.com/news/home/20230321005525/en/New-Research-Uncovers-a-Developer-Experience-Gap-for-Provisioning-Environments-Resulting-in-Modern-Application-Deployment-Delays)
- Shadow IT grows annually
- Developers leave for competitors

❌ **"Free-for-All Self-Service"**
- Monthly surprise bills from AWS and Azure
- 43 Azure Subscriptions or Payer Accounts, nobody knows why
- "Who deployed this?" - Everyone, daily

✅ **The Reality: It's a Spectrum** Every workload needs self-service. The question is HOW MUCH.

**Your opportunity:**
- **Innovation workloads:** 20% automation (baseline governance)
- **Emerging patterns:** 60% automation (guided flexibility)
- **Core operations:** 95% automation (full standardization)

_Most organizations only apply self-service to core workloads, leaving 70% of the opportunity on the table_

### Speaker Notes (Mike):

"Show of hands - who here has said 'self-service doesn't work for our innovative teams'? [pause] Right, most of you.

Here's what you're missing: Cigna thought the same thing. Then they realized their AI/ML teams were spending $300K monthly on ungoverned GPU instances because they had zero self-service. Not full automation - just ZERO path forward.

Now those same teams use lightweight self-service - they get flexibility to experiment, but with automatic tagging, budget alerts, and data residency controls. Their cloud spend dropped 40% and they ship models twice as fast.

The myth isn't whether to do self-service. It's thinking it has to be all or nothing."

---

## **SLIDE: The Forces That Determine Your Self-Service Level**

### Slide Title: **Stop Fighting These Forces - Orchestrate Them**

### Visual: Spectrum with real examples plotted

**What Drives Self-Service Decisions:**

← **Need Flexibility** | **Need Automation** →

**Your Workloads Live Everywhere:**

- **R&D Project (20% automated):** Unknown patterns, rapid pivots, expert users
- **Mobile App Backend (95% automated):** 10M users, PCI compliance, zero variance tolerated
- **Legacy App + AI Module (60% automated):** Stable core, volatile edges, mixed teams

**The Key Insight:** These aren't opposing forces - they're requirements to balance:

- **High change rate?** Add governance, not gates
- **High compliance?** Encode rules, not reviews
- **Expert users?** Give them guardrails, not handcuffs

### Speaker Notes (Auggy):

"Notice something? That mobile app at 95% automation and that R&D project at 20% could exist in the same company, same day, both correct. PNC has exactly this - their payment processing is fully automated, their blockchain experiments are minimally governed. Both use self-service, just different flavors.

The expensive mistake is forcing one level everywhere. Your CISO wants maximum control everywhere, your developers want maximum freedom everywhere. The answer? Match the level to the work, not the org chart."

---

## **SLIDE: Self-Service Isn't Just for Production Workloads**

### Slide Title: **CloudBolt Capabilities Across the Spectrum**

### Content:

**Innovation/Experimental (20-40% Automated)** _What they still need:_

- ✓ Account vending & automatic RBAC setup
- ✓ Baseline tagging for cost attribution
- ✓ Approved firewall rules & IP ranges
- ✓ Data classification policies
- ✓ Automatic shutdown for idle resources
- ✓ Budget alerts before the $100K surprise

**Emerging Patterns (40-70% Automated)** _Starting to standardize:_

- ✓ Lifecycle policies (TTL, patch schedules)
- ✓ Monitoring package auto-deployment
- ✓ Guided templates with flex parameters
- ✓ Environment promotion workflows
- ✓ Compliance scanning on deploy
- ✓ Multi-cloud placement logic

**Core Operations (70-95% Automated)** _Full governance required:_

- ✓ Zero-touch deployment via pipeline
- ✓ Dynamic workload placement
- ✓ Policy-as-code enforcement
- ✓ Automatic remediation
- ✓ Cost optimization built-in
- ✓ Full audit trail & compliance reporting

**Bottom line:** _Even your most experimental teams need SOME automation - even if it's just "don't let me accidentally spend $1M"_