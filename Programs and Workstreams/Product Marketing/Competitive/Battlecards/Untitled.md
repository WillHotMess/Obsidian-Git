Cloudbolt/NordCloud Optimisation Deep Dive

Callum Murrell with Nordcloud Oy
Recorded on May 7, 2025 via Microsoft Teams, 51m



Participants

CloudBolt Software
Callum Murrell, Sr. Cloud FinOps Solution Engineer
Peter Easler
Yasmin Rajabi, Chief Strategy Officer

Nordcloud Oy
Marek Lipinski, Capacity/Finops Lead

Other
Marcin.Walkow
B Arvind Kumar
Saswata Roy
Zbigniew Pazdan
Souradeep Khasnobis



Transcript

0:01 | Marcin.Walkow
good afternoon. 

0:01 | Callum
How's everybody doing? 

0:07 | Callum
She always interrupts at the weirdest times. 

0:14 | Marcin.Walkow
It does. Yes… everybody. 

0:19 | Callum
All right. This afternoon. 

0:22 | Marek
Hello? Hey, Marek. Hi. 

0:33 | Callum
People joining? Hey, Yasmin. Hey, Peter. 

0:41 | Peter
Hey, everybody. 

0:44 | Callum
Brilliant. Hello. Hey, srideep. 

1:00 | Callum
Right. Marek. Are we waiting on anybody else from your? 

1:04 | Marek
Side? I don't think so. Zb, if he joins, he'll join from his car, but he said he's not essential today, yeah. 

1:12 | Callum
We've. 

1:12 | Marek
got a commercial call. 

1:13 | Callum
Tomorrow, I replied to you guys. We've got that scheduled. All right. Well, thank you very much for joining everybody. So, the purpose of the call today is really to dive into and kind of complete the kind of suite of demos that we've been doing for cloudbolt finops platform, and we'll be focusing on the kind of the new optimization capabilities in this session. So kind of continuous optimization policy driven automation, and also kubernetes, optimization and rightsizing as well. I think those are the kind of the key main areas. Any other areas that you'd like to dive into or any other clarification that you'd need from the previous calls? 

2:01 | Marek
I don't have questions to the previous calls. At least. I think one of the questions I asked in the email was about the GDPR thing for the european union. And because I think you wrote that the data is stored in the UK, I think that's not a problem currently isn't it, it's. 

2:18 | Callum
there's. 

2:19 | Marek
some kind of a law that. 

2:22 | Callum
Yeah, we're fully GDPR compliant. And in any case, you know, if it was a requirement for you guys that the data had to be hosted in Europe, we would be able to make that work. 

2:35 | Marek
Okay. So, I think that was the one thing not confirmed and that was for those guys that you will have a call with tomorrow, so. 

2:43 | Callum
Yeah, no worries. I can talk through the GDPR implications and stuff. Tomorrow. No problem. Okay. All right. Well, in that case, I think I'm going to hand things over to Peter who's going to walk through the continuous optimization capability of the platform. 

3:05 | Peter
Yeah, Peter? 

3:06 | Callum
You? Okay. Awesome. 

3:14 | Peter
Everybody got my screen. All right. 

3:18 | B Arvind Kumar
Yep. Cool. 

3:19 | Peter
So, similar to yesterday, there's a lot to this. I want to make sure we have time to kind of dive into the kubernetes, just because of the value that a lot of our customers have gotten out of that. But to kind of get a little bit of context from your side, you know, similar to yesterday and the billing configurations, you know, how you guys do the tiered rating, what those use cases look like, how it varies, if you could kind of help me get a good understanding of how your team or folks in your business, kind of identify opportunities for finops services. You know, do you have customers coming to you with broad or specific requests? Do you have, you know, kind of packaged offerings, things like that can kind of help me better point and walk through how different customers similar to yourselves would use the tool? 

4:20 | Marek
So, we have a service called managed finops, led by Marcin who's on this call actually the custom. And we also have, you know, we can do also finops projects if the customers approach us to do some kind of an optimization project for them. Managed finops is quite a big, bigger engagement for a couple of years where we help the customers, you know, to optimize to do the tagging and everything around that. But, yeah, so we use, we can do it with a tool or without a tool as well. Yeah, of course, it's better with, yeah. 

5:09 | Peter
And you guys typically start with an assessment of some sort, you know, kind of getting a broad understanding of. 

5:16 | Marek
Yeah, we put finops advisors and they do a kind of maturity assessment, initially check where the client is at and then we build a strategy around it. 

5:27 | Peter
Okay. So, yeah, we've you know, since I started with cloudbolt, we've had numerous different service providers kind of approach it in different ways. Some that want to use cloudbolt for those assessments. You know, kind of what we looked at yesterday with the export reports, being able to plug that in and, you know, in a day or so be able to produce something that serves a good baseline understanding of cost trends, what's driving the cost? You know, what accounts are driving the cost tagging consistency as well as a baseline level of waste identification. You know, where we have opportunities for power scheduling, decommissioning, rightsizing license utilization, things like that. So, we've… also had a lot of service providers whose assessments that they were already doing were much more comprehensive than this they were doing, you know, interviews with teams and, you know, had something more than we can get out of the box. Again, this is taking the data we have as it is and pulling it out and summarizing it. And there's a lot of customization we can do with this. But where I think a lot of our customers have kind of more success is similar to your guys' resale business where, you know, all of the scope of potential customers are already coming through. We're doing the re, rating everything like that as they, you know, kind of expose the default views to customers of, you know, dashboards and cost reports and budgets, et cetera. Customers will, you know, see potential savings and look for assistance and how do we start to drive that? So what we've aimed to enable with the continuous optimization is going kind of beyond the old… way of, you know, and I can even show it in our legacy tool of, you know, we're looking at a list of recommendations that can be, you know, pulled out to the excel or, you know, there's some workflow things in here. They've been here maybe for 10 days or hundreds of days and it's you know, still a very manual kind of resource consuming process where either users in your org or the customer's org are coming through and, you know, point by point identifying pushing them onto application teams, et cetera. You know, the new way of approach with the continuous optimization is we want to provide to the end users whether it's an application owner, a, you know, developer, someone ultimately responsible for managing these underlying resources. We want to give them the ability to really specify within their scope and their context, what is waste? What is an idle server is in a production environment? You know, do we want to be looking at a month plus rather than, you know, a couple weeks? Do we want to consider ram for certain workloads and other workloads? You know, we're just looking at cpu kind of getting beyond that one size fits all approach. So as we get into actually pursuing those recommendations looking to remediate, you know, we don't need to continuously look backward and validate whether the thresholds and the rules that got that recommendation generated were relevant. So the waste signal, the waste signal concept really allows for, you know, multiple different identifiers triggers for what is an idle server or a database or, you know, storage or, you know, IP configuration and those kind of exist within our global waste signal list. And then as we look at policies, those users can then say, all right, if waste signal, a B and C hits for our volume servers, databases, if… those waste signals fire within X scope. So my accounts or my groups or, you know, environment or application matching in my area, what are the events that we want to trigger based on that? So again getting away from the kind of point and click going through a list of recommendations to, this is a continuous thing. If, you know, a 30 day trigger goes off on a waste signal for servers and then Aws and azure scope, we want a approval notification to go out, you know, via slack or teams or email or, you know, a custom webhook, or we want a payload of information to be delivered into, you know, ServiceNow or an itsm platform. And as those checks start getting completed, then we have an ultimate event. And that can be something as simple as again a second payload of data with the resource id, you know, current SKU, proposed SKU, or, you know, subscription id, account id, all the information you need to take an action within, you know, a standard change management process or we can start to look at actual resource actions, powering off the machine, terminating or deleting unattached volumes or disks, adding a tag to a resource. So in that next patching cycle, it gets picked up, you know, trying to have a broad dynamic approach. We understand, not all customers are going to approach this the same way. But we want to essentially put a process out there that enables either low maturity or high maturity, finops, users to, you know, have a repeatable ongoing process that lowers the human intervention required. So that's the long and short of it. Obviously, you know, how you guys kind of interact with this with the customers can be as simple as exposing this out to customers and kind of handling them through the process to, you know, owning it on your end and putting policies in place, that kind of drive recommendations into, you know, your internal recommendation processes. 

11:42 | Peter
I covered a lot there. Any questions off the bat? 

11:50 | Marek
No questions for me… all. 

11:54 | Peter
Right. So, one of the key benefits of these policies of the, you know, continuous as soon as that waste signifiers were, you know, action, a chain of actions is being taken and the KPIs, we can really drive off this are much more effective in telling them, you know, the standard, what's your efficiency or your optimization score, you know, which is just looking at potential savings divided by total cost. Now, we can look at things like insight to action time, you know, from the moment a waste signal is fired, IE, a resource in an environment was considered to be, you know, idle or unoptimized. How long is it taking for an action to be taken? That action doesn't necessarily mean that resource is turned off. That could mean a tag was added. That could mean the recommendation was rejected, but just kind of showing that, you know, we're getting away from this, you know, this ec ii has been up running probably two percent cpu for 160 days at the 20 day mark that got flagged as idle. So we want not only the Roi to be easily, you know, identifiable, but we want the kind of duration and the time and efficiency we got to that Roi to be easily telling. And that gives our service providers the ability to kind of go back and easily quantify, you know, the value of that finops service. We're rolling out more KPIs that we can get into as well around kind of more cumulative indexes looking at insight to action versus commit use discount coverage scores and allocation and tagging scores that we'll be rolling into the new platform here over the next couple months. 

13:49 | Marek
I think this looks good. Yeah, go ahead, saswata. Yeah. 

13:54 | Saswata
Just one thing from a previous session. So, in one of the sessions, we saw that there was a document that was available or it was generating sort of a document that gave us a brief summary on the entire optimization scope. So how do you generate from here and how does it look like at the end? 

14:15 | Peter
Yep. So that export report is something? 

14:24 | Peter
That's generated kind of as a point in time look, it probably falls more into that bucket of the older way of doing things. But for an assessment for a cumulative approach, it can be super valuable especially as a POC with customers or showing finance, executive leadership teams or app owners, department owners, what the potential is within their environment. So, you know, either in that excel or that powerpoint report, we can have, you know, a full breakdown of some of the operational potential savings and operational is going to be, you know, where we have opportunities to turn off power, schedule, right? Size virtual machines, databases, you know, cleanup on attached disks, and then more business focused, which will be the RI and savings plan potential. So this comes out of the box with these export reports and you know, either medium that you want to be used… and all recommendations can also be pulled out via API. So if you have kind of your own reporting, you want to push these into Power BI, or, you know, a tableau report or directly into Jira, you know, that can be programmed and set up via the API too. 

15:43 | Saswata
Thank you. Just a follow up on this topic. So is it also possible to set up like tenants for separate areas of tenants for the customers where we can carry all such reports for them to see on a specific interval of time? 

15:59 | Peter
Yep. The tenant and Iam structure applies across the board. So, you know, beyond just cost reports and everything, if a customer or if a user logs into a specific tenant switches over to, you know, customer B, they will just see the savings associated with customer, said customer. And within the kind of global admin, Nord cloud tenant, every page will have similar group or group tag based filters. So, you know, if you want to see in your global view, what customers one two and three have… available, you can just like that here. 

16:56 | Peter
Similarly with the policies, those can obviously be spoke scoped to customers. 

17:09 | Peter
Yeah. So I'll kind of segue into another area. So we've obviously had recommendations, you know, and a finops approach for a long time with the older way of doing things, the newer way of doing things. It's still very focused on… cloud native infrastructure, our virtual machines, databases, storage, we, you know, our customer base and kind of the market and analysts we work with. There's always been a high ask for, you know, more advanced modernized coverage and our optimization scope. You know, how can we look at kubernetes or, you know, license based or PaaS services? And that really drove us to partnering and ultimately combining with stormforge to provide a well. I'll let Yasmin get exactly how valuable it is. But essentially, you know, we're not going to rebuild the wheel within cloudbolt. There are organized orgs like stormforge, who is now a part of cloudbolt that have handled, you know, well, I'll just pass it to Yasmin. 

18:23 | Yasmin
I mean, you do a great job Peter. But the, I mean, part of why cloudbolt acquired stormforge was because the same kind of continuous optimization approach that the cloudbolt platform has in its DNA is applicable with stormforge as well where we collect all the kubernetes metrics in near real time. So like every 30 seconds, we're collecting metrics using machine learning to analyze what the resources need, and then setting the proper requests and limits so that you're not under provision but you're not over provision. So it's just right. You can put in a lot of input into the machine learning to say like, hey, I want to be more aggressive more on the saving side or I want to be more conservative on the reliability side and every individual workload gets its own model. So the requests and limits, the patches themselves are for each container. So if you have one workload with one container, you get a patch that has one set of requests and limits. If you have a workload with five containers, then you get the right requests and limits per container because it's been looking at the usage patterns and then forecasting the right recommendations. And then we have the automation to go make that real. Whether we're patching the workload directly, whether you're deploying the recommendations through some CI CD through a webhook, any means that make sense? The software allow you to do that? 

19:43 | Peter
Yeah, I'd say the benefits twofold, you know, in addition to the continuous optimization in kubernetes, which we obviously never had the ability to even look below a cluster level scope with kubernetes, workloads, regardless of, you know, if it's eks, aks on Prem or bare metal, we now also have the ability to use that data to do much more relevant and accurate cost distribution cost allocation. If, you know, your customers are running a handful of kubernetes workloads that ultimately are serving 10, 20 different applications and they want to distribute the total cost of those clusters out… to the applications based on their job usage, their consumption against the capacity. We now have that data. We don't need to do it just, you know, proportionally based on the total cost of account a versus B versus C. And some of the things I'm talking about are coming, you know, a lot of what I'm showing obviously is already here but. 

21:00 | Peter
You guys this? 

21:01 | Marek
Is, yeah, this is very promising. I think looks good. I'm not sure. Marcin, do you recall us having our finops customers using kubernetes? 

21:16 | Marcin.Walkow
In a sense of a big portfolio, like over an industry standard, rather negligible, or at least on the enterprise grade level, it's not that prevalent on a startup level. Yes, on SMB, maybe on enterprise, it really depends on the business case. And I don't put much emphasis into allocating namespaces or other, you know, like generally thinking about clusters in a sense of cost allocation or others because you just start using carpenter and majority of your problems are solved. And then you move maybe to other bits but not at least on our end, giving an extensive answer. 

22:06 | Yasmin
And if it helps, we work really well with carpenter or automode, where oftentimes Aws is pulling us into customer environments because carpenter is awesome, but it operates at the node level. And if your pods are over provisioned, then there's only so much. You can scale down at the node level because you still have all the waste and that's the hard problem we work with a lot of like large financial enterprises and that's where their challenges come out. So, if you do kind of come into an environment where they have deployed carpenter and they haven't gotten all the savings. We have some recorded videos, case studies with Aws on how, right sizing the pods with the stormforge helps. 

22:46 | Marcin.Walkow
And I think it's spot on Jasmin, as you pointed out, and you brought a very specific yet an isolated case which is financial institution because they use spots or they can use kubernetes for that or fargate, you know, eks, whatever the point is that this would be applicable to this specific industry case. And if you go to CPG which is running sap or data analytics workloads, then 90 percent of their costs will be bound to everything which has to let's say be kind of old school. This would be VMS and that's it. And so I get the point but it's kind of limited. At least my exposition is different. You may have, you know, a bigger exposition which I appreciate that's not the case here. 

23:36 | Yasmin
Yeah, no, it makes sense. We have traditionally been very kubernetes focused because that's all we did. Now that we're part of cloudbolt. It's how do we take that same approach of machine learning based rightsizing to the rest of cloud infrastructure? So that's what we're excited about because we also had customers that are like cool. You're doing kubernetes, can you do everything else? And we're like, well, no, we're focused on kubernetes? But now that we have access, that is kind of the next step here as the products come together. 

24:08 | Marek
Cool. 

24:09 | Marcin.Walkow
Let's move on. 

24:18 | Peter
I've covered a majority of what I wanted to, from kind of the process, what it looks like for different types of customers. Were there any specific questions of stuff we covered? Callum? Anything I missed? 

24:34 | Callum
No, I think you've kind of covered most of it, Peter. I think really what we kind of wanted to show you guys in this session was just kind of some of the optimization capabilities that you can have with the tool and well, so show you the kind of the full suite of optimization capabilities. So I know that you were talking about wanting to build out kind of services out to your customers and how you can, so cloud can be customized so that you can kind of pick and choose which modules you want to enable for customers and which customers you want to kind of enable everything for. So we kind of wanted to just show you everything you kind of pick and choose what would make most sense for your customers. Can you see how you could use some of these services or all of these services even across some of your customers? 

25:21 | Marek
Oh, definitely. So, so Peter, you're asking about our finops, but, we do recommendations and optimization recommendations kind of reports for our kappa resell customers as well. So if we can hide stuff great. But maybe there's a potential also to, you know, change, our normal service a little bit, with the help of cloudbolt. So, so, yeah. 

25:49 | Callum
Absolutely. So you'll get access to all of these capabilities within the tool as kind of standard really. And with the exception of perhaps, the kubernetes optimization, which is an extra add on. So your team will be able to see all of this, all these recommendations as kind of standard. And then you'll be able to also then kind of write your reports, use the export report functionality to generate reports for your customers. But you'll then also then be able to give customers access to those to cloudbolt and see as Peter showed you yesterday in terms of report profiles to be able to hide or expose the margins of discounts, the re, rating that you're doing in the platform and then base the recommendations that Peter's just shown you on those kind of re rated metrics, so that they can see, they might see different optimization figures to what you can see, you might, you can pull everything back to a higher level. That could also be a like a kind of a unique selling point for a cloud server, a finops service, if you can kind of pass down better rates and optimize kind of the full stack and they can only see part of it. So, I think there are a number of different ways you can offer services there. 

27:01 | Marek
I think for sure. Yeah. 

27:05 | B Arvind Kumar
I have a inquisitive question here. 

27:09 | B Arvind Kumar
So, Peter, when we actually look into. 

27:11 | B Arvind Kumar
the tool, we often get questions like what would be the Roi, if, based on the current span, we move to a reserved instance. 

27:20 | B Arvind Kumar
Or a savings plan. So, is that? 

27:22 | B Arvind Kumar
Some kind of thing which is already available in built on cloudbolt or what, how is it? 

27:31 | Peter
Yep. Yeah. We have… rinsp reporting essentially covering off recommendations… for additional investment in reservations or savings plans across Aws and azure right now. We don't have GCP but that's on the roadmap. We also have analysis on existing inventory where utilization stands, you know, based on or per RI per SP, per service type per account. The recommendations we look at what the native recommendations are what Aws trusted advisor says, and then what azure advisor says. And then we essentially pair that against or aggregate against what we identify in our service advisors. If we see that there's out of the 100 percent of compute, we see that 15 percent of it's running idle could be right sides could be changed. We want to pair that against and ensure we're not just recommending to right, you know, preserve everything off the bat for three years that's kind of where you get into some trouble that one of our other partners can help with. But yeah, we do have recommendations for all that. 

28:50 | B Arvind Kumar
I was more looking at it from an Roi perspective. So no problem, that we generally do it from using curve files as to if I know the savings from the trusted advisors. OK, this is the expected savings. But in order to achieve that savings, what is the holding period as investments which goes in? So they will recover the costs only starting twelfth month or ninth month, that kind of a calculation is something we often get such queries. So no, never mind. 

29:26 | Peter
Yeah. I see what you're saying. A lot of our customers have just switched to, the monthly billing cycle with ris and savings plans to get out of the all up front purchases. Obviously, there's still a commitment there of you're making those monthly payments. But yeah, otherwise, in terms of looking at the curve, obviously, we have the ability to look at like retail on demand costs of all the usage that we see. So, you know, we can look at unblended costs versus retail on demand versus, you know, amortized costs and kind of show as reservations are purchased, what's the daily weekly monthly, you know, savings that are actually being captured. 

30:19 | B Arvind Kumar
Okay. 

30:22 | Callum
We are, also, I think exposing through our partner ecosystem in the new platform kind… of third party integrations with regards to commitment management. So, I think our chair is one of those that we're going to be exposing to the partner ecosystem shortly. And that has precisely, I think what you're talking about in terms of looking at say like… showing the overview of the existing ris and savings plans in a customer environment and then saying, you know, if a customer were to purchase, you know, xri, they would break even or they would see this return on investment on, you know, over this timeframe over a y timeframe. So that functionality, yeah, commitment management as Peter's showing you right now, you know, we have the data in the curve but it's not our kind of bread and butter. It's not our strong suit, you know? So we're really going to be leaning into the partner ecosystem and kind of trying to surface kind of the best of brand in the commitment management space through cloudbolt. So customers can manage their ris and savings plans and commitments alongside all of their infrastructure in cloudbolt. 

31:42 | Callum
Okay. 

31:43 | Marek
Okay. 

31:45 | Callum
Peter, did I miss anything there? I think I covered. Yeah. So guys, I mean, I realized that we're kind of halfway through the session and we've kind of covered most of the optimization capability. Where would you like to go next? Do you have any kind of more technical questions that we can answer with regard to the platform, the capabilities, any services that you might be thinking about offering out to your customers? What can we help you with? 

32:17 | Marek
Do you guys have anything maybe related to green ops or sustainability or anything like that? No? 

32:27 | Callum
Not currently, we've done some. 

32:30 | Peter
Yeah, we've done one offs with customers that need that. So we've done it. It's not something out of the box but we have done. 

32:42 | Marek
Yeah. 

32:42 | Peter
Done work with like pulling from the azure, the Aws sustainability endpoints and including them in, you know, the exports here or in like a Power BI template or something like that? 

32:56 | Marek
Yeah. Okay. Thanks. Yeah. I guess the question is because we were asked by some customers about this. So, yeah, I guess it's getting more popular. 

33:12 | Callum
If the scalers really start giving kind of detailed sustainability metrics that we can measure, it's, very difficult. And any kind of startup that says that they're kind of doing sustainability isn't really doing that much. They're still just extrapolating the cost data. So, you know, once the hyperscalers start giving us like a measurable data point, then we can absolutely build it into the platform and it will be something that we look to pivot to quite soon quite quickly once that's available. But right now, they like to just say, oh, cost is a great proxy for sustainability. So, everything that you see in the market about sustainability at the moment is just kind of repackaging those cost metrics to try and kind of make you more efficient, which in a sense is true but it's not looking, you know, there are very few ways to get that kind of depth at the moment, but it is something that we're looking to move into as soon as the metrics are available. 

34:09 | Marek
Thanks. 

34:16 | Zbigniew
I. 

34:16 | Marek
hope you. 

34:16 | Zbigniew
Guys can hear me because I'm in my car. Yes, I do have one question which might have been answered already Marek. So stop me if it was data residency and security concerning the UK region because we have a growing customer base of government and financial institutions in the UK which are very picky about no data leaving the UK soil. Is that doable? There's a checkmark on that? 

34:46 | Callum
Yeah, that's absolutely doable. So currently all the data is hosted in Aws London. So no data. So everything's kind of running in Aws London and we're completely GDPR compliant. So, yeah, that's not a problem. And if, you know, for the same, you know, if you had european customers that required data to be hosted in Europe, that also wouldn't be a problem, but we are also compliant with GDPR in Europe as well. 

35:22 | Callum
Okay. Guys. Well, if you didn't have any more questions, I think we can wrap this call up early. I know we've got a commercial call tomorrow afternoon to start running through things on that front, but just a final call. Did you have any more technical questions? Anything that the team here can help you with before we talk commercials tomorrow… would you like to? 

35:51 | Marek
Discuss? I mean, yeah, but, yeah. 

35:53 | Callum
Would there be a kind of a next step technically, would you like to kind of, you know, do a proof of concept? Would you like to see a demo of the product in your own environment? You know, what would be kind of the next step for you to get to grips with things? Yeah. 

36:07 | Marek
That would be good. I guess if we could play around in it as well? 

36:15 | Marcin.Walkow
Do we have to use our data in order to run a demo or you can provide us with a demo instance like other providers sometimes do and, you know, just have a place to play around. So. 

36:27 | Callum
In order to do kind of like a proof of concept, it would need to be your data. Currently in our demo instance, we're using all of our production data. So it, you wouldn't have any of the kind of the right capabilities or anything like that. So it's much better to kind of hook it up to your data. Also that's part of the proof of concept. Well, it's part of one of the, I guess good things to show is how easy it is to connect new customers in. So getting familiar with kind of, you know, onboarding new customers, onboarding new data to the platform, seeing that data and then manipulating it is kind of a key area that lots of MSPS in particular want to be able to test. 

37:09 | Marcin.Walkow
Let it be okay. I mean we deploy different tools as well. And the key is not about deploying but rather getting approvals plus some security folks saying yes from the practice. So that's why I'm asking whether you have a tenant with a demo data, dummy data like so called rather than we have to run through our internal procurement. This will take time and it may mean weeks. So I would like to have something within days if it's applicable. If it's not applicable, that's fine point taken that's okay. 

37:42 | Peter
Yeah, I'd say it's definitely worth getting that process kicked off. We do have a sandbox environment we can get access to. 

37:53 | Marcin.Walkow
It doesn't have to be a huge data. We can get recommendations anyways or cost allocation on a 30,000,000 scale or 100 dollar scale. It would be exactly the same process. The point is only to understand from the team. Like Arvind today asked a question, you know, about the Roi just to figure. Okay. So are there all the means that we can cover? Or maybe we need to have some kind of a custom tweaks using API binding some with some external data and so on. And so on. And while, you know, on a call, we can go through your flow, most probably will have a different one as every customer have a different flow. So that's why I'm a little pressuring you on this because I'm pretty sure that there will be some questions like follow up. We can do it via email, but the point is to get some, you know, feeling, of this tooling. 

38:45 | Peter
Yeah… I think it was a couple of days to work out which environment would be best. And to your point, yeah, it'll be scaled down but we'll give you the ability to click through everything you've seen in the last two days, just about everything. Some of the new platform stuff may not be there, but. 

39:08 | Marcin.Walkow
It's fine. We are for the core features, not the gadgets, no worries. 

39:14 | B Arvind Kumar
But all said and done, one question which I had initially yesterday as well was on the onboarding, if at all we get started with cloudbolt, how easy or hard or how difficult will it be for moving on to cloudbolt? That is something we have to be clear about because that's also an effort and there will be people involved from both the parties. So how that is helped or how that is done from your end? That is also something we should be clear about. Yeah. 

39:52 | Peter
Yeah, it's a great question. And in my opinion, it's very easy that vary that you can vary primarily depending on who on the customer side we need and if, and how long it takes us to get them. But ultimately, it's going to be very standard permission sets, very standard onboarding process. You know, once we have the read access, cloudformation templates deployed, you know, typically kers already exists there's already, you know, the data we need is already there from a cost perspective. So, typically, if we were to kick off tomorrow and have, you know, our goal would be to be fully moved over and onboarded within a month. Typically, that can be, you know, closer to a week, or two, it kind of depends on the amount of customers, the… amount of customers, the amount of different cloud environments, but, you know, we've moved over, you know, a service provider had 200, 300 customers across the Aws azure to GCP, we had 95 percent of them done in, you know, two days. And then there's the ones that stretch out where the service provider, the reseller doesn't have access to those last five, 10 percent of customers to do it. So, we work with those next level down customers to, you know, either use existing roles, deploy new roles and pull it into cloudbolt. 

41:18 | B Arvind Kumar
And, this will also handle all the GDPR related issues, right? So, because, many customers in UK, in like, we have restrictions from India, some customers had to be handled from Poland. So that kind of GDPR restrictions also get handled during the onboarding, right? Yeah. Okay. 

41:43 | Marcin.Walkow
That's an interesting question. Do you mean that? Okay, and I guess I understand where Arvind is coming from. So, let's say we have, 100 customers, 10 of them, their data cannot be seen by the eyes of anybody who isn't sitting, you know, let's say in a GDPR compliant region, I would just call it this way. Question is, about the accesses, is it correct? Arvind? Do you mean this that's right? 

42:12 | B Arvind Kumar
Yes, yes, yes. I mean this because that kind of restriction is it's what to say essential because, we are bound by the contracts that we can't see it. So, if we are in the GDPR compliant location, we have visibility and if not, we don't but when we talk about the administration of the tool as such, there, we will have some permissions which would be different from the viewing permissions. So, these kind of these kind of ifs and buts will definitely come, during onboarding. 

42:49 | Peter
Yeah, obviously, different regions have their different restrictions and policies, things like that. I will say that fortunately and unfortunately, sometimes there's nothing new to us, whether it's you know, our human resources being able to travel, you know, having Calum, and different support staff, in India and the states, you know, we've worked with a lot of government entities in the states and abroad that have similar types of restrictions, so that typically, you know, nothing in that is going to be new to us or, you know, a big red flag, but we'll be, adapt as adaptable as you need us to be, I guess is what I'm saying. 

43:34 | B Arvind Kumar
So, that leads to another question though, I'm sorry, I'm just dragging it a bit more. What would be the service availability as in there, there can be some issues regarding the tool which we encounter while servicing our customers or servicing our internal stakeholders. So, what's the service say, mode of operations from your end? Is it a service desk or is it an email trigger or is it some ticketing system which you have within… all? 

44:11 | Peter
Of the above in that first month or so of engagement in the rollover, the, you know, you would have direct access beyond just the ticketing and support desk. We obviously try and build out best practices of starting there. But in the immediate, you know, we're moving customers over. We got to get things fixed ASAP, and Callum can obviously talk through, you know, our premier support levels, what 24 seven looks like? What? Having a dedicated tam looks like, you know, to help kind of interface between support. If it's more than just a bug, you know, working with our product team with our services team, if there's you know, new builds or things like that. So different… optionality. But yeah, okay. 

44:56 | B Arvind Kumar
But you have a process in place for a support thing, right? So, we don't have to struggle to look for support, no. 

45:08 | Marcin.Walkow
From the process side, last question, let's say we want to onboard 100 customers in Aws, it means that you provide us with the cloudformation or any type of a definition of policies and roles that you expect. On your end, we have to deploy them. Once seen. You can start ingesting the data, right in a high level box. Yeah. Okay. I guess that, do you have like two types of accesses like billing data, access, S tree and metrics, data that you're ingesting standard stuff? Okay? You can ingest both focus and non focus data, right? Okay. And I guess we need to specify what lies in this S tree or blob or whatever, right? At the point of onboarding. 

46:00 | Peter
Yeah, by default, for, the bill ops, the billing configuration, all that if we were to again start this tomorrow, we would start with all the non focus data. Okay? Focus data would be used for the new data platform. So there'll be a transition phase in there. We wouldn't there wouldn't be a need to have every customer set up to right off the bat by any means. 

46:27 | Marcin.Walkow
Okay. And last, but not least, is there any possibility because we are like we are a hybrid cloud provider, which means that we have also some angle on, I mean, we as a group. Okay? So sometimes there may be cases like this. Primarily we're a public cloud base, but let's imagine a situation like this. I have a cost allocation angle that I need to enrich focus data. You can enrich it with on premises data, right? There is a common data scheme where we can add, you know, certain line items, how easy it is to do it. So that I would understand that this is a on premises piece in cloudbolt. 

47:13 | Peter
Yeah. So we've actually already built that out, I guess depending on the depending on the exact type of on premise workload, but we have an agent that can go into a VM where a… red hat openshift, I'll have to check exactly on what's available today, but that agent fetches that utilization data and does that conversion into the focus format. 

47:48 | Marcin.Walkow
Okay. So without the agent, is it possible to add, those costs anyway? I mean, because imagine you get this from let's say somebody who is doing this capex thing and you have a set, of information that you would just to add as a cost not specifically around the agents because like, yeah, there may be like two separate streams like running agent can be a data thing in just, you know, we don't want to mingle with that. Sure. 

48:17 | Peter
We would need to scope out exactly what it looks like. That is been one of the key points as to why we went down this route to begin with. So that door could be open of ingesting for if the data matches at least partial format of focus, we can get it in. You know, we didn't have support for oracle two weeks ago. And now we did, you know, last year that would have taken two to three months just kind of rebuilding a new support for that. So I can't give exact specifics on what that would look like. But. 

48:54 | Marcin.Walkow
Okay. But is it just possible right now via API to add some data or we are limited to those providers and they're like ingested data and would require some hacking, let's say adding to existing one, you know, a CSV. Okay. Good. Okay. If you have a roadmap of. So this is my last question. It's a generic question. What are the known things that, you know, that you're developing which aren't in the tool and we can expect them, which means a roadmap. Do you have a roadmap public one or semi confidential? Let's say bounce or NDA that you can share? 

49:33 | Callum
Yeah. We do. I'd probably organize like another call probably with our CTO to run through a roadmap in detail with you and he would be able to talk through some of the things that are coming over the next kind of six to 12 months and kind of beyond because there's quite an aggressive kind of delivery timeline that's happening over the next kind of six months in particular. And then in the further future, we're kind of pivoting quite heavily. Okay? 

50:03 | Marcin.Walkow
So the point is not to hold you accountable to your roadmap. The point is only to understand. Okay. So procure this, let's say, you know, we'll start onboarding. We just need to have some kind of a strategic overview because this one is highly tactical, very good though, you know, one step above just to understand. Okay. So those are the limitations. We have a service like this. It means we need to prepare that's the point clearly. Yeah. 

50:28 | Callum
Absolutely. We can absolutely share that kind of horizon scanning with you. 

50:32 | Marcin.Walkow
Awesome. Thank you. No more nagging from my side. 

50:36 | Callum
By all means nag away. It's good to keep us honest… cool. Say. 

50:44 | Marek
One hour was enough. 

50:48 | B Arvind Kumar
That's. 

50:49 | Callum
just the right amount of time. Any further questions, guys… we'll. 

50:57 | Marek
definitely. Talk about it. You know, if anything pops up, we'll send you an email. Yeah. 

51:06 | Callum
We've got the commercial call tomorrow, I think so. We'll touch base then, but, yeah, any further technical questions, please do get in touch. Happy to answer anything by email and again, happy to jump on into another call and drill into things. And tomorrow, we can also talk about a proof of concept and getting you access to a demo instance in a sandbox as well. 

51:29 | Marek
Okay. Sounds good. Okay. Sounds good. 

51:34 | Callum
Brilliant. Thank you very much, guys. Cheers. 

51:36 | Marek
Thank you. Bye. 