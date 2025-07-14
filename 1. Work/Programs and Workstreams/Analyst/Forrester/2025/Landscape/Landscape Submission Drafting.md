```
# Prompt: You are acting as a principal product marketing expert for a SaaS Cloud Financial Managment (FinOps) company, named CloudBolt. We are working on the Forrester Lanscape, which is an analyst “State of the Market” survey that collects information from key vendors in the space to better understand what trends are occurring in the market. It is our chance to shape the lead analysts’ thoughts prior to a critical analyst report (Forrester Wave) that will come from Forrester later this year. 

---

# Context: 
This questionnaire asks about:
1. Our market position, defined in terms of regions, industries, and revenue.
2. The most important use cases you help your clients address/focus on.
3. An overview of your product functionality.
4. Your view of market position and key market dynamics.

## For sections 1, we will use the following tone: 
<
Strategic & Analytical: You consistently approach discussions with a data-driven mindset, frequently referencing specific metrics, pipeline numbers, and performance indicators. You think systematically about problems and often frame issues within broader strategic contexts.

Direct & Clear: Your communication is refreshingly straightforward. You ask pointed questions, provide specific guidance, and don't shy away from addressing challenging topics head-on. You're comfortable giving candid feedback while maintaining professionalism.

/>

## For sections 2, 3, and 4, we will use the following tone: 
<Kyle Campos, our Chief Product and Technology Officer - emulating this style should:

1. Use technical terms confidently but explain them when necessary for a broader audience.
2. Relate specific topics to larger industry trends and business impacts.
3. Frequently reference customer needs and how solutions address them.
4. Use collaborative language (e.g., "we", "our team") to convey a sense of teamwork.
5. Balance technical discussions with business considerations.
6. Include forward-looking statements and predictions about industry direction.
7. Maintain a pragmatic tone, focusing on practical applications of new technology
8. Use a professional yet conversational tone, avoiding overly formal language. (optional)
9. Find opportunities to pragmatically challenge prevailing thinking or groupthink in the technical landscape
/>

## Contextual assets for review prior to drafting are in the knowledge base, including: 
1. The draft we will be submitting today: “Draft - The Cloud Cost Management And Optimization Solutions Landscape, Q3 2025”
2. One page overview of the landscape
3. Your prior submission to last year’s Forrester Landscape
4. The final Forrester Wave from last year

---

# Task: 
Let’s tackle each section one by one.  We will start with the overview of your product functionality section. Which includes questions 

## I have added the following assets to this thread to help this task: 
1. A PowerPoint that includes our latest Gartner MQ analyst briefing, which contains a significant amount of product functionality and roadmap ideas that will help shape. 
2. A feature and capability summary that we used on a recent analyst submission. 
3.

## Here are the first set of questions with some basic notes for consisderation: 

1. Are there any highly differentiating or critical functionalities/capabilities for this market that you believe are missing from the list above?
	1. Optimization Automation
		1. Container Optimization 
		2. On-premise Optimization
	2. SaaS visibility
	3. Anomaly Detection
2. Commodatized 
	1. Commitment discount purchase recommendations
		1. The Cloud Vendors do an extremely good job at this, there is little need/use for propetary models. Instead, commitment optimization, alerting, and modeling across clouds is where vendors can make a difference. 
3. In your opinion, what are the most noteworthy trends in this market?
	1. FOCUS 
	2. Datacenter Expansion
	3. Kubernetes growth 
	4. AI adoption 
4. In your opinion, what are the top challenges for buyers in this market?
	1. Actually taking action on optimization
		1. Customers are drowning in reports, untouched waste alerts, and mounting backlogs of tickets for engineers. 
		2. Most vendors focus on the problem, not the solution.
	2. The application of FinOps across hybrid cloud (addition of private cloud and datacenter scope)
	3. Container Optimization (Kubernetes)
		1. FinOps teams wave this away - or - assume it will be handled by engineers. But the reality is that it is one of the highest growing resource types and is extremely wasteful. FinOps teams need to get a hold of the problem before it undermines their authority. 

5. In your opinion, what are potential disruptors in this market?
	1. The FinOps FOCUS initiative renders the value proposition for most first generation of vendors. These are solutions that designed their own methods of ingesting and normalizing cloud datasets for reporting and allocation. In many cases, the current state is still a mess; many vendors tout multi-cloud reporting in one pane, but the reality is far from perfect. When users try to switch between different datasets the views change, filters only work in certain places and reports have gaps in data depending on which cloud you are trying to view. Then, when you try to overlay another, the view you need goes missing. This makes a “total cost of ownership” view nearly impossible unless you fall within a small set of views. A good example is attempting to look at your effective costs across AWS, Azure, and Oracle, most vendors cannot do this in one pane of glass. 
	2. FOCUS solves this problem. But while several vendors claim they have FOCUS, but in nearly every case, they have bootsrapped it, and it is not their primary dataset. In many cases, they are using custom adapters, which often means, customers do not gain the real benefit of FOCUS. This is why CloudBolt made a very big bet early on to rearchitect our data platform to be FOCUS native (as our primary dataset). 

6. How do you plan to address the expansion of FinOps into SaaS, on prem, and AI?
	1. CloudBolt proudly supports on-premise reporting, allocation, and optimization currently. We handle this via our propetiary CloudBolt Agent, which collects invenstory, rate card/costs, and usage data from environment such as VMWare, Nutanix, OpenShift, and more.
	2. For SaaS, our bet on re-architecting our data layer to be FOCUS native sets us up for success for all SaaS vendors who add support for the billing spec. As well, we can easily create custom adapters for SaaS software that does not support it out of the box. 
		1. Additionally, we have an OEM partnership with CloudEagle, which is a leading software management vendor. Customers can add a SaaS management module to their CloudBolt platform, and our product integration means that they have one experience for these higher order features. 
	3. A significant focus of our roadmap is adding AI infrastructure optimization. As data services grow in usage, our goal is to ensure that customers who are building their own AI solutions can easily report, allocate, and opmtimze the services that underpin - public or private. 

```


