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

