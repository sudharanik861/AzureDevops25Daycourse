
# Day 2 - Q&A: Service Models & Deployment Models

---

## Service Model Questions

**Q1: What is the difference between IaaS, PaaS, and SaaS in simple terms?**
IaaS = you rent a raw computer and do everything yourself. PaaS = you rent a ready-made platform and just deploy your code. SaaS = you rent finished software and just use it.

**Q2: Give one Azure example for each service model.**
IaaS = Azure Virtual Machines. PaaS = Azure App Service. SaaS = Microsoft 365.

**Q3: Which service model should a developer choose to deploy a Python web app without managing servers?**
PaaS (Azure App Service) — it handles OS, Python runtime, scaling, and SSL. Developer only writes and pushes code.

**Q4: What is the Shared Responsibility Model?**
It defines what the customer manages vs what the cloud provider manages. In IaaS, customer manages most. In SaaS, provider manages everything. It's a sliding scale of responsibility.

**Q5: Can a company use IaaS and PaaS together?**
Yes. Very common. Example: Azure VM (IaaS) for legacy database + Azure App Service (PaaS) for new web app. Both connect within the same Azure Virtual Network.

**Q6: What is lift-and-shift migration?**
Moving an application to cloud without changing its code. You create a VM in cloud with the same OS and config as your on-prem server, then copy the application. This is an IaaS approach.

**Q7: What is vendor lock-in?**
When your app depends heavily on one provider's proprietary services, making it expensive and difficult to switch providers. Example: Using Azure-specific services that have no equivalent on AWS.

**Q8: Is PaaS always better than IaaS?**
No. IaaS is better for legacy apps, custom OS needs, GPU workloads, and specific compliance configurations. PaaS is better for new apps where you want to move fast.

**Q9: How does pricing differ between the three models?**
IaaS = per VM per hour (₹5-50/hour). PaaS = per app instance or per request (starts free). SaaS = per user per month (₹200-1500/user/month).

**Q10: What is serverless? Is it a 4th service model?**
Serverless (like Azure Functions) is a subset of PaaS. You write functions instead of full apps. You pay only when your code runs — zero cost when idle. You still don't manage servers.

---

## Deployment Model Questions

**Q11: What is the difference between Public and Private cloud?**
Public = shared infrastructure, accessed over internet, pay-per-use (Azure, AWS). Private = dedicated to one organization, full control, can be on-prem or hosted.

**Q12: Give a real-world example of Hybrid Cloud.**
Apollo Hospitals: patient records on private cloud (compliance), appointment booking website on Azure public cloud (auto-scaling). Connected via secure VPN.

**Q13: What is Multi-Cloud? Why use it?**
Using 2+ cloud providers together. Reasons: avoid vendor lock-in, use best service from each, redundancy if one goes down. Example: Netflix uses AWS + GCP.

**Q14: Which deployment model is most secure?**
Private cloud gives the most control. But public cloud providers invest billions in security — a well-configured public cloud can be more secure than a poorly managed private data center. Security depends on implementation.

**Q15: What is Azure Arc?**
Azure Arc is Microsoft's hybrid cloud service. It lets you manage on-prem servers, Kubernetes clusters, and databases from the Azure portal — as if they were Azure resources.

**Q16: What is Azure ExpressRoute?**
A dedicated private connection between your on-prem data center and Azure. Unlike VPN (which goes over public internet), ExpressRoute provides a direct link — faster, more reliable, and more secure.

**Q17: Why would a hospital use Hybrid Cloud instead of just Private Cloud?**
Pure private cloud can't handle sudden traffic spikes (like during a pandemic when everyone books online appointments). Hybrid lets them keep sensitive data private while using public cloud for website scaling.

**Q18: What is data residency? Why does it matter?**
Data residency means your data must be stored within a specific country's borders. Example: RBI mandates that Indian financial data stays in India. This drives the choice of private or region-specific public cloud.

**Q19: Can a startup use Private Cloud?**
Technically yes, but it's not practical. Private cloud needs large upfront investment and an IT team. Startups benefit from public cloud — no upfront cost, auto-scaling, and managed services.

**Q20: What is the difference between Hybrid Cloud and Multi-Cloud?**
Hybrid = one organization using private + public cloud together (split by workload). Multi-Cloud = one organization using multiple public cloud providers (Azure + AWS + GCP).

---

## Scenario-Based Questions

**Q21: A company wants to migrate an old .NET app running on Windows Server 2008 to cloud without changing code. What should they use?**
IaaS (Azure VM) with Windows Server 2008 image. This is a lift-and-shift migration. Deployment model: Public cloud (unless compliance requires private).

**Q22: A 5-person startup wants to build a mobile app backend. They have no IT budget. What model and deployment?**
Service model: PaaS (Azure App Service or Azure Functions). Deployment: Public cloud. Reason: No upfront cost, auto-scaling, managed platform.

**Q23: Indian Army needs to host a classified communications system. What should they use?**
Service model: IaaS (full control over OS and security). Deployment: Private cloud (on-premises, air-gapped from internet).

**Q24: An e-commerce company gets 50x traffic during Diwali sale. They need to scale for 5 days and go back to normal after. What cloud model?**
Public cloud with auto-scaling. They can spin up 50x more servers for the sale period and scale down after. Pay only for the 5-day spike.

**Q25: A company uses Azure for their website but wants to use AWS for machine learning. What is this?**
Multi-Cloud strategy. They use the best service from each provider — Azure for web hosting, AWS SageMaker for ML.
