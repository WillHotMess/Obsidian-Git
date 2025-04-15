# Competitors
## FinOps 
- Cloudability
- CloudCheckr
- CloudHealth

## Workflows
> Post MOFU Submission | Follow-up & List enrollment

- **GigaOM Radar_Report**
	- Delete Entirely 
- **Comparison Guide_CloudHealth**
	- CloudBolt Software\Team Marketing - Documents\Creatives\Competitive guide
- **Comparison Guide_Morpheus**
	- CloudBolt Software\Team Marketing - Documents\Creatives\Competitive guide
- **Comparison Guide_Cloudcheckr**
	- CloudBolt Software\Team Marketing - Documents\Creatives\Competitive guide
- **Comparison Guide_Cloudability**
	- CloudBolt Software\Team Marketing - Documents\Creatives\Competitive guide


https://app.hubspot.com/contacts/214114/record/0-1/49170269/

Soft bounced

Rejected by recipient's email security filter

SENDING_DOMAIN_MISCONFIGURATION smtp;550 5.7.133 RESOLVER.RST.SenderNotAuthenticatedForGroup; authentication required; Delivery restriction check failed because the sender was not authenticated when sending to this groupThe From address domain doesn't authorize HubSpot to send on its behalf, ask your IT team to check DKIM or SPF.

--- 

**Kas,** 

I am auditing our competitive guides this afternoon for an upcoming refresh and am seeing that many submissions are soft-bouncing due to the following error: 

> Rejected by recipient's email security filter
> SENDING_DOMAIN_MISCONFIGURATION smtp;550 5.7.133 RESOLVER.RST.SenderNotAuthenticatedForGroup; authentication required; Delivery restriction check failed because the sender was not authenticated when sending to this groupThe From address domain doesn't authorize HubSpot to send on its behalf, ask your IT team to check DKIM or SP

You can review a ton of examples of this **[HERE](https://app.hubspot.com/email/214114/details/169455607571/recipients/sent)**

--- 

In case you need it, this is how I understand our current MOFU architecture.  
1. Competitive guides are behind a gated MOFU form: there is a single, shared, form, for the following:  
	- Analyst reports (all)
	- Competitive Guides (all)
	- CII Research Reports (some)
	- Webinar Recordings (some)
	- Whitepapers (some)
2. Then, a HubSpot workflow parses which page the user converted on and runs an automation branch
	- You can review that logic, [**HERE**](https://app.hubspot.com/workflows/214114/platform/flow/590677313/metrics?showVersions=true&revisionStartTimestamp=1732053148709&revisionEndTimestamp=1744565645320&version=75&changedActions=&rangeType=CUSTOM&startDate=2024-11-19&endDate=2025-04-13)
3. Then a pre-written email is sent to the customer with the relevant link to the asset. 

**Can you please dig in as soon as possible and see if this an issue?
