**Marketing Email Cadences for Optimize Live Trial Users**

Overview
# Signup Sequence
[Engagement Studio](https://pi.pardot.com/engagementStudio/studio#/30561/reporting) \- Ops setup, reporting
Email Copy:
* [Activate: Sign up](#bookmark=id.gn5ao2v393mw)  
  * [Template in Pardot](https://pi.pardot.com/emailTemplate/read/id/43231)  
  * Sends after signup

* [Activate: Sign up, no install](#bookmark=id.qmw0xvjyhhuq) \- reminder 1  
  * [Template in Pardot](https://pi.pardot.com/emailTemplate/read?id=57388)  
  * Wait 2 days and send if no install  
      
* [Activate: Sign up, no install](#bookmark=id.qmw0xvjyhhuq) \- reminder 2  
  * [Template in Pardot](https://pi.pardot.com/emailTemplate/read?id=57400)  
  * Wait 5 days and send if no install

# Installed Sequence

[Engagement Studio](https://pi.pardot.com/engagementStudio/studio#/24904/reporting) \- Ops setup, reporting

Email copy:

* [Apply Recommendations: Preliminary Recommendations are ready](#bookmark=id.lxd4d8f1ku76)   
  * [Template in Pardot](https://pi.pardot.com/emailTemplate/read/id/43225)  
  * Sends after install 

* [Apply Recommendations: Complete Recommendations are ready to apply](#bookmark=id.u581xg2fdza5)  
  * [Template in Pardot](https://pi.pardot.com/emailTemplate/read/id/43228)  
  * Sends after 7 days

* [Convert: Trial ending soon \- recommendations applied](#bookmark=id.cxltdhp2xtua)  
  * [Template in Pardot](https://pi.pardot.com/emailTemplate/read?id=43273)  
  * Sends after 21 days

* [Convert: Trial ending soon \- recommendations NOT applied](#bookmark=id.30vfn2c5o8rh)  
  * [Template in Pardot](https://pi.pardot.com/emailTemplate/read/id/43276)  
  * Sends 2 days before trial ends

# Signup Sequence Email Copy

## **Activate** [(back to top)](#bookmark=id.n240y7ubv7jy)

* [Sign up](https://pi.pardot.com/emailTemplate/read/id/43231)  
  * *Can view in the \#user-alerts Slack channel*

***Send right after signup***

From: StormForge | yasmin@email.stormforge.io

Subject Line: Getting Started with Your StormForge free trial

Preheader: What you need to start continuously rightsizing

Body: 

Welcome to your free trial of Optimize Live\!

In order to start rightsizing workloads, you need to [install the agent](https://app.stormforge.io/getting-started) on a cluster. 

Our agent is read only, we do not collect any personal data directly. See our [Security FAQ](https://docs.stormforge.io/optimize-live/reference/faq-security/) for details on the [data](https://docs.stormforge.io/optimize-live/reference/faq-security/#what-data-do-you-collect) and [metrics](https://docs.stormforge.io/optimize-live/reference/faq-security/#metrics) we collect (we are SOC 2 Type II compliant). 

Installing takes less than 2 minutes → [Watch how](https://www.stormforge.io/videos/getting-started-optimize-live-install/?utm_source=Pardot&utm_medium=email&utm_campaign=trial-signup)

In ten minutes, you’ll get an overview of your waste and performance risk with preliminary rightsizing recommendations for all your workloads. 

Don’t have a test cluster? No worries\! Play around in the [sandbox environment](https://app.stormforge.io/sandbox?utm_source=Pardot&utm_medium=email&utm_campaign=trial-signup) to try it without installing.

Let me know you have any questions, or you can [email support](mailto:support@stormforge.io), or [send a message in the product](https://app.stormforge.io?support).

Best,  
Yasmin Rajabi  
VP of Product

## **Activate** [(back to top)](#bookmark=id.n240y7ubv7jy)

***Send 2 business days after signup and no installation***

StormForge | yasmin@email.stormforge.io

Subject Line: Reminder: Install a cluster to start rightsizing

Body:

In order to start identifying waste and performance risks that you can address with continuous rightsizing, you need to install the StormForge agent on a cluster. It takes less than 2 minutes. [Watch this 15-second video](https://www.stormforge.io/videos/getting-started-optimize-live-install/?utm_source=Pardot&utm_medium=email&utm_campaign=trial-signup) to walk through the process. 

Once you install, you’ll get an overview of your waste and performance risk with preliminary rightsizing recommendations for all your workloads in ten minutes. 

Let me know you have any questions. You can also [email our support team](mailto:support@stormforge.io), or [ask a question directly in the app](https://app.stormforge.io?support).

Best,  
Yasmin Rajabi  
VP of Product

## **Activate** [(back to top)](#bookmark=id.n240y7ubv7jy)

***Send 5 business days after signup and no installation***

StormForge | yasmin@email.stormforge.io

Subject Line: Reminder about your StormForge trial

Body:

I noticed that you haven’t installed a cluster yet to start your [StormForge Optimize Live trial](https://app.stormforge.io/?utm_source=Pardot&utm_medium=email&utm_campaign=trial-signup). It takes less than 2 minutes, and you’ll be on your way to continuously rightsizing waste and performance risk away. Walk through the process in [this 15-second video](https://www.stormforge.io/videos/getting-started-optimize-live-install/?utm_source=Pardot&utm_medium=email&utm_campaign=trial-signup). 

Our team is here to help if you have any questions. You can [email support](mailto:support@stormforge.io), or [ask a question directly in the app](https://app.stormforge.io?support).

Best,  
Yasmin Rajabi  
VP of Product

# Install Sequence Email Copy

## **Apply Recommendations** [(back to top)](#bookmark=id.n240y7ubv7jy)

* [Preliminary recommendations are ready](https://pi.pardot.com/emailTemplate/read/id/43225)

StormForge | yasmin@email.stormforge.io

Subject Line: Your preliminary recommendations are ready

Body:

We have good news\! Your preliminary recommendations are ready\! 

Here’s what comes next:

1. [Login](https://app.stormforge.io/) to your Optimize Live trial instance  
2. Navigate to your Clusters  
3. Review the preliminary recommendations to see our initial rightsizing opportunities	  
4. In about 7 days, your preliminary recommendations will be solidified. We will send you an email when that happens. At that point you will be able to apply your recommendations.

If you’d like to speak with the StormForge technical team about your preliminary recommendations, please contact us at [support@stormforge.io](mailto:support@stormforge.io).

As a reminder, you can only add one cluster to your trial instance.

Thank you,

The StormForge Team

## **Apply Recommendations** [(back to top)](#bookmark=id.n240y7ubv7jy)

* [Recommendations are ready to apply](https://pi.pardot.com/emailTemplate/read/id/43228)  
  * *Could schedule for 7 days after agent install*

***APPROVED***  
***Send 7 days after signup and installation***

StormForge | yasmin@email.stormforge.io

Subject Line: Your rightsizing recommendations are ready to apply

Body:

We have good news\! Your complete recommendations are now ready for review. Here’s what comes next:

1. [Login](https://app.stormforge.io/) to your trial instance  
2. Navigate to your Clusters  
3. Review the recommendations and the financial impact  
4. When ready, apply the recommendations  
   * To apply a recommendation you can install the applier, use our CLI to apply it, or export the patch for use with kubectl instructions to do so are [here](https://docs.stormforge.io/optimize-live/getting-started/view-apply/#applying-workload-recommendations)

If you’d like to speak with the StormForge technical team about your recommendations before applying them, please contact us at [support@stormforge.io](mailto:support@stormforge.io).

.

Thank you,

The StormForge Team

***Send 14 days after signup and installation***

StormForge | yasmin@email.stormforge.io

Subject Line: Deploying recommendations with GitOpsYour rightsizing recommendations are ready to apply

Body:

Are you using GitOps tools in your environment? The StormForge Applier works alongside these tools to ensure the state of your workloads.We have good news\! Your complete recommendations are now ready for review. Here’s what comes next:

5. [Login](https://app.stormforge.io/) to your trial instance  
6. Navigate to your Clusters  
7. Review the recommendations and the financial impact  
8. When ready, apply the recommendations  
   * To apply a recommendation you can install the applier, use our CLI to apply it, or export the patch for use with kubectl instructions to do so are [here](https://docs.stormforge.io/optimize-live/getting-started/view-apply/#applying-workload-recommendations)

If you’d like to speak with the StormForge technical team about your recommendations before applying them, please contact us at [support@stormforge.io](mailto:support@stormforge.io).

Thank you,

The StormForge Team

## **Convert** [(back to top)](#bookmark=id.n240y7ubv7jy)

* [Trial ending soon \- recommendations applied](https://pi.pardot.com/emailTemplate/read?id=43273)

StormForge | yasmin@email.stormforge.io

Subject Line: Your trial ends soon, how’s it going?

Body:

In order to keep having StormForge Optimize Live automatically offer rightsizing recommendations on your trial cluster, and all additional clusters you have in K8s, you will need to upgrade your account. 

To learn more about pricing, please contact our sales team at [sales@stormforge.io](mailto:sales@stormforge.io).

Thank you,

The StormForge Team

## **Convert** [(back to top)](#bookmark=id.n240y7ubv7jy)

* [Trial ending soon](https://pi.pardot.com/emailTemplate/read/id/43276)   
* Send two days before trial ends

StormForge | yasmin@email.stormforge.io

Subject Line: 	Your trial ends soon, do you need more time?

Body:  
Your StormForge Optimize Live trial ends in two days\!

Do you need more time to apply your recommendations?

If you’d like to speak with the StormForge technical team about your recommendations before applying them, please contact us at [support@stormforge.io](mailto:support@stormforge.io).

Thank you,

The StormForge Team

---
# Email Drafts
### Immediate: Welcome Email

```
From: William Norton <WNorton@cloudbolt.io>
Subject: Welcome to StormForge! Your account is ready

Hi [First Name],

Welcome to StormForge! I'm excited you've taken this step toward optimizing your Kubernetes environments.

To get started:

1. **Install StormForge in your cluster**
   Use our Helm chart with this simple command:
helm install stormforge stormforge/optimize-live --namespace stormforge --create-namespace

[Detailed Installation Guide] [Installation Video]

2. **Security FAQ**
• StormForge runs entirely within your cluster
• We use read-only metrics collection by default
• All data is encrypted in transit and at rest
• [Full Security Documentation]

3. **What to expect**
• Initial analysis begins immediately after installation
• Preliminary recommendations appear within 24 hours
• Complete optimization recommendations in 7 days

Once you've completed installation, you'll receive an email confirming that StormForge is running and analyzing your environment.

Need help? Our team is ready to assist:
[Contact Support]

Welcome aboard!

William Norton
Vice President of Product Marketing
CloudBolt Software
```


## Path A: Users Who Don't Install

### Day 2: First Installation Reminder

```
From: William Norton <WNorton@cloudbolt.io>
Subject: Your StormForge optimization journey awaits - Quick installation guide

Hi [First Name],

Thanks for signing up for StormForge! I noticed you haven't completed installation yet, and I wanted to make sure you have everything you need to get started.

Kubernetes optimization doesn't have to be complex - StormForge makes it simple with our ML-powered platform that automatically right-sizes your resources and reduces cloud costs.

Here's a quick installation video (under 4 minutes) that walks you through the process:
[Installation Video Link]

Need the written instructions instead?
[View Installation Guide]

Questions about security or implementation? Our installation is designed to be non-disruptive and secure - initially operating in observation-only mode so you can see potential savings before making any changes.

Need help? Our engineering team is standing by.
[Schedule Installation Support]

Looking forward to seeing your optimization results!

William Norton
Vice President of Product Marketing
CloudBolt Software
```

### Day 3: Case Study Email

```
From: William Norton <WNorton@cloudbolt.io>
Subject: How Acquia achieved 65% cost reduction with StormForge

Hi [First Name],

I wanted to share a success story that might help illustrate why getting StormForge installed is worth your time.

Acquia, a leading digital experience platform provider, was struggling with efficiently allocating compute resources across thousands of customer applications while migrating from VMs to Kubernetes.

After implementing StormForge, they achieved remarkable results:
- 65% cost reduction through workload optimization
- 99.99% availability maintained across their platform
- 55% faster EKS migration (reduced from 18 to 8 months)

As Ed Brennan, Acquia's Chief Software Architect, put it: "We needed something that could keep up with the pace of scale that we have. Within the first six months of deploying Optimize Live, we achieved the ROI we wanted."

Ready to see what StormForge can do for your environment?
[Install Now - 15 Minutes or Less]

Need some guidance? Our team is happy to help with a guided installation.
[Schedule 30-Min Installation Support]

Here for you,
William Norton
Vice President of Product Marketing
CloudBolt Software
```

### Day 5: Second Installation Reminder

```
From: William Norton <WNorton@cloudbolt.io>
Subject: Still interested in optimizing your Kubernetes costs?

Hi [First Name],

I wanted to check in as I noticed you haven't installed StormForge yet. Many of our users discover they're overspending on Kubernetes by 40-70% - money that could be redirected to innovation rather than overprovisioned resources.

Common installation questions:

1. "Is it complicated to install?"
   Not at all - it takes about 15 minutes using Helm, and we have a video walkthrough.
   [Quick Install Video]

2. "Will it impact my running applications?"
   StormForge starts in observation-only mode, analyzing your workloads without making changes until you're ready.

3. "Do I need specialized skills?"
   If you can install a Helm chart, you're all set! No machine learning expertise required.

I'm also happy to connect you with our support team who can help with installation:
[Book Installation Support Call]

Looking forward to helping you optimize your Kubernetes spend!

William Norton
Vice President of Product Marketing
CloudBolt Software
```

### Day 10: Expert Tips Email

```
From: William Norton <WNorton@cloudbolt.io>
Subject: 3 Kubernetes cost-saving tips from our engineers

Hi [First Name],

Even though you haven't installed StormForge yet, I wanted to share some actionable Kubernetes optimization tips from our engineering team:

1. **Review your CPU requests vs. actual usage**
   Most organizations overprovision by 200-300%. Check your Prometheus metrics to identify your largest gaps.

2. **Adjust your Horizontal Pod Autoscaler settings**
   The default target utilization (80%) often leads to inefficient scaling. Consider testing a higher threshold for non-critical workloads.

3. **Consider namespace-level resource quotas**
   Implementing quotas can prevent "resource sprawl" and create better accountability across teams.

These manual methods can help, but StormForge's ML-powered automation takes optimization further by continuously adapting to your specific workload patterns.

Ready to see the difference automation can make?
[Install StormForge in 15 Minutes]

Still have questions? I'm happy to connect you with our technical team:
[Schedule a Conversation]

Best regards,

William Norton
Vice President of Product Marketing
CloudBolt Software
```

### Day 20: Final Reminder

```
From: William Norton <WNorton@cloudbolt.io>
Subject: Last chance to activate your StormForge trial

Hi [First Name],

I noticed your StormForge trial hasn't been activated yet, and I wanted to check in one last time.

If you're still looking to optimize your Kubernetes costs, you're not alone. Our data shows that the average organization can reduce container costs by 40-70% through proper optimization.

What makes StormForge different:
• Machine learning that adapts to your specific workload patterns
• Automated right-sizing without performance risks
• Full control through customizable guardrails and policies

We're seeing organizations struggle with rising cloud costs, and Kubernetes is often the least optimized part of their infrastructure. If that resonates with you, I'd love to help.

[Install StormForge - Final Opportunity]

Or if you'd prefer a personalized approach:
[Request a Guided Demo]

Thank you for your interest in StormForge. If we don't hear from you, we'll add you to our general CloudBolt newsletter with cloud optimization insights.

William Norton
Vice President of Product Marketing
CloudBolt Software
```

## Path B: Users Who Install

### Day 1: Preliminary Recommendations Email

```
From: William Norton <WNorton@cloudbolt.io>
Subject: Your StormForge installation is working! Initial insights inside

Hi [First Name],

Great news! StormForge is successfully installed and has begun analyzing your Kubernetes environment. We're already generating preliminary insights based on your workload patterns.

Next Steps:
1. [Link] Explore your StormForge dashboard
2. [Link] Review the workloads being analyzed
3. [Link] Configure any additional namespaces you'd like to include

Over the next 7 days, StormForge's machine learning will continue analyzing your workload patterns to generate comprehensive optimization recommendations. The longer StormForge runs, the more accurate and valuable these recommendations become.

Questions about what you're seeing? Our team is here to help:
[Schedule a Platform Walkthrough]

Looking forward to sharing your complete recommendations soon!

William Norton
Vice President of Product Marketing
CloudBolt Software
```

### Day 7: Complete Recommendations Email

```
From: William Norton <WNorton@cloudbolt.io>
Subject: Your optimization recommendations are ready - See your potential savings

Hi [First Name],

Exciting news! After a week of analyzing your Kubernetes environment, StormForge has generated complete optimization recommendations for your workloads.

These aren't generic recommendations – they're precisely calibrated to your specific workload patterns using our machine learning engine.

Ready to implement these changes? You have options:
• One-click application through our dashboard
• Export as Kubernetes YAML for your CI/CD pipeline
• Use our GitOps integration

Want to discuss these recommendations with our team?
[Schedule an Optimization Strategy Call]

Remember: These recommendations are just the beginning. StormForge continuously adapts to changes in your workload patterns for ongoing optimization.

William Norton
Vice President of Product Marketing
CloudBolt Software
```

### Day 14: GitOps Integration Email

```
From: William Norton <WNorton@cloudbolt.io>
Subject: Automate your Kubernetes optimization with GitOps

Hi [First Name],

I hope you've had a chance to review your StormForge optimization recommendations. Today, I wanted to highlight how you can seamlessly integrate StormForge with your existing GitOps workflows.

For teams using GitOps for Kubernetes management, StormForge offers several integration options:

1. **Direct Git Repository Integration**
   Automatically create pull requests with optimization changes
   [Setup GitOps Integration]

2. **CI/CD Pipeline Integration**
   Include StormForge in your existing deployment workflows
   [CI/CD Configuration Guide]

3. **Periodic Export**
   Schedule regular YAML exports to apply on your schedule
   [Configure Export Schedule]

By integrating StormForge with your GitOps workflow, you get:
• Full visibility into all optimization changes
• Consistent approval processes for all environment changes
• Automatic version control and audit history
• Seamless rollbacks if needed

Need help setting this up? Our engineers are available to assist:
[Schedule GitOps Integration Support]

Already implementing your recommendations? I'd love to hear about your results!

William Norton
Vice President of Product Marketing
CloudBolt Software
```

### Day 21: Success Story + Upgrade Email

```
From: William Norton <WNorton@cloudbolt.io>
Subject: Take your Kubernetes optimization to the next level

Hi [First Name],

You've been using StormForge for about three weeks now, and I hope you're seeing the benefits of ML-powered Kubernetes optimization. I wanted to share how another customer expanded their success beyond the trial.

Acquia, a digital experience platform provider, started with a focused implementation similar to yours. After seeing early results, they expanded StormForge across their environment and achieved:

- 65% cost reduction through workload optimization
- 99.99% availability maintained across their platform
- 55% accelerated EKS migration (from 18 to 8 months)
- Automated daily optimization of resources across thousands of customer applications

As their Chief Software Architect noted: "Within the first six months of deploying Optimize Live, we achieved the ROI that we wanted to achieve, and we have continued to optimize that over time."

Ready to expand these benefits across your entire infrastructure?

[Upgrade to StormForge Pro]

Or if you'd like to discuss enterprise options with our team:
[Schedule a Conversation]

Still exploring? Here's a quick checklist to ensure you're getting the most from your trial:
- Have you applied any of your recommended optimizations?
- Have you configured guardrails for your specific requirements?
- Have you explored our GitOps integration?

Let me know if you have any questions!

William Norton
Vice President of Product Marketing
CloudBolt Software
```

### Day 28: Final Engagement Email

```
From: William Norton <WNorton@cloudbolt.io>
Subject: Your StormForge trial is ending soon - Next steps

Hi [First Name],

Your StormForge trial is coming to an end soon, and I wanted to check in about your experience so far. I hope you've seen the value of ML-powered Kubernetes optimization in your environment.

Based on the data from your environment, StormForge has identified potential annual savings. As you consider next steps, here are your options:

1. **Upgrade to StormForge Pro**
   • Unlimited workload optimization
   • Advanced guardrails and policies
   • Priority technical support
   • Integration with CloudBolt's comprehensive FinOps platform
   [Upgrade Now]

2. **Explore Enterprise Options**
   • Multi-cluster management
   • Custom integration services
   • Dedicated account management
   • Training and implementation support
   [Talk to Sales]

3. **Extend Your Trial**
   Need more time to evaluate? We're happy to extend your trial for an additional two weeks.
   [Request Extension]

If you choose not to continue with StormForge, your trial will expire soon, but we'll maintain your account data for 30 days should you decide to return.

I'd love to hear about your experience with StormForge, regardless of your decision. Feel free to reply to this email with any feedback.

William Norton
Vice President of Product Marketing
CloudBolt Software
```
