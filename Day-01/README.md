# Day 1 - Introduction to Cloud Computing

## Learning Objectives
- Understand what cloud computing is and why businesses use it
- Learn the 5 essential characteristics of cloud computing
- Understand Cloud Service Models (IaaS, PaaS, SaaS)
- Understand Cloud Deployment Models (Public, Private, Hybrid)
- Learn about CapEx vs OpEx
- Understand the basics of Virtualization

---

## 1. What is Cloud Computing?

Cloud computing is the delivery of computing services — servers, storage, databases, networking, software — over the internet ("the cloud") on a pay-as-you-go basis.

**Analogy:** Owning a generator vs. plugging into the electricity grid. You don't build a power plant — you pay for what you use.

### Why Cloud Computing?
- No need to buy expensive hardware upfront
- No need to hire a large IT team for maintenance
- Access resources from anywhere in the world
- Scale up or down based on demand
- Pay only for what you use

---

## 2. Five Characteristics of Cloud Computing (NIST Definition)

| Characteristic | Meaning | Example |
|---|---|---|
| On-demand self-service | Get resources instantly without calling support | Spin up a VM from Azure Portal |
| Broad network access | Access from any device, anywhere | Use Azure from phone, laptop, tablet |
| Resource pooling | Multiple users share the same physical infrastructure | Azure serves millions of customers from same data centers |
| Rapid elasticity | Scale up/down quickly based on demand | Add 100 servers during Diwali sale, remove after |
| Measured service | Pay only for what you consume | Billed per hour, per GB, per request |

---

## 3. Cloud Service Models

### IaaS (Infrastructure as a Service)
- Provider gives you: Virtual machines, storage, networking
- You manage: OS, runtime, applications, data
- Example: **Azure Virtual Machines, AWS EC2**
- Analogy: Renting a kitchen — you get the oven and fridge, but you cook yourself

### PaaS (Platform as a Service)
- Provider gives you: Everything except your app and data
- You manage: Only your application code and data
- Example: **Azure App Service, Google App Engine**
- Analogy: Take-and-bake pizza — dough and toppings are ready, you just assemble and bake

### SaaS (Software as a Service)
- Provider gives you: Everything — fully managed software
- You manage: Nothing, just use the software
- Example: **Microsoft 365, Gmail, Salesforce**
- Analogy: Pizza delivery — just open the box and eat

### Responsibility Matrix

| Layer | IaaS | PaaS | SaaS |
|---|---|---|---|
| Application | You | You | Provider |
| Data | You | You | Provider |
| Runtime | You | Provider | Provider |
| Middleware | You | Provider | Provider |
| OS | You | Provider | Provider |
| Virtualization | Provider | Provider | Provider |
| Servers | Provider | Provider | Provider |
| Storage | Provider | Provider | Provider |
| Networking | Provider | Provider | Provider |

> **Key Rule:** As you move from IaaS → PaaS → SaaS, your responsibility decreases.

---

## 4. Cloud Deployment Models

### Public Cloud
- Owned and operated by a third-party cloud provider
- Shared across multiple organizations over the internet
- No upfront cost, pay-as-you-go
- Example: **Microsoft Azure, AWS, Google Cloud**

### Private Cloud
- Exclusively used by a single organization
- Can be hosted on-premises or by a third-party
- Offers more control, security, and compliance
- Example: **Azure Stack, on-premises data center**

### Hybrid Cloud
- Combination of Public + Private cloud
- Sensitive data stays on private cloud, scalable workloads go to public cloud
- Example: **Azure Arc**

### Community Cloud
- Shared by several organizations with common requirements (compliance, security)
- Example: Cloud shared by multiple government agencies

### Real-World Scenario
> A hospital stores patient records on a **private cloud** (for compliance and security) but runs its appointment booking website on a **public cloud** (to handle traffic spikes). This is a **hybrid cloud** approach.

---

## 5. Advantages of Cloud Computing

| Advantage | Description |
|---|---|
| Cost Savings | No hardware purchase, shift from CapEx to OpEx |
| Scalability | Scale up/down in minutes based on demand |
| Reliability | Built-in backups, disaster recovery across regions |
| Speed | Provision new resources in minutes, not weeks |
| Global Reach | Azure has 60+ regions worldwide |
| Security | Enterprise-grade security managed by the provider |

### CapEx vs OpEx

| | CapEx (Traditional IT) | OpEx (Cloud) |
|---|---|---|
| **Full Form** | Capital Expenditure | Operational Expenditure |
| **What** | Buy servers upfront | Pay monthly subscription |
| **Cost** | Large upfront investment | Small recurring payments |
| **Risk** | Hardware depreciates over 3-5 years | Cancel anytime |
| **Analogy** | Buying a car | Using Ola/Uber |

---

## 6. Virtualization

### What is Virtualization?
Virtualization is the technology that allows you to create multiple virtual machines (VMs) from a single physical server using software called a **Hypervisor**.

### What is a Hypervisor?
A hypervisor is software that sits between physical hardware and virtual machines. It allocates CPU, memory, and storage to each VM.

### Types of Hypervisors

| | Type 1 (Bare-metal) | Type 2 (Hosted) |
|---|---|---|
| **Runs on** | Directly on hardware | On top of an existing OS |
| **Performance** | Faster, more efficient | Slower, extra OS layer |
| **Used for** | Data centers, production | Development, testing |
| **Examples** | Hyper-V, VMware ESXi | VirtualBox, VMware Workstation |

### Benefits of Virtualization
- **Better utilization** — One physical server runs multiple VMs
- **Cost savings** — Fewer physical servers needed
- **Isolation** — Each VM is independent; if one crashes, others are safe
- **Easy backup** — Snapshots can save the state of a VM instantly
- **Fast provisioning** — Create a new VM in minutes

### How Virtualization Connects to Cloud Computing
> Virtualization is the **foundation** of cloud computing. Cloud providers like Azure use virtualization to divide massive physical infrastructure into smaller virtual resources that customers rent on-demand.

---

## Q&A - Day 1

### Cloud Computing Basics
**Q1: What is cloud computing?**
Cloud computing is the delivery of computing services (servers, storage, databases, networking, software) over the internet on a pay-as-you-go basis.

**Q2: What is the electricity grid analogy for cloud?**
Just like you don't build a power plant to get electricity — you plug into the grid and pay per unit — in cloud computing, you don't buy servers, you rent computing power and pay for usage.

**Q3: Name the 5 characteristics of cloud computing.**
On-demand self-service, broad network access, resource pooling, rapid elasticity, and measured service.

### Service Models
**Q4: What is the difference between IaaS, PaaS, and SaaS?**
IaaS = you manage OS and above. PaaS = you manage only app and data. SaaS = provider manages everything. Moving from IaaS to SaaS, your responsibility decreases.

**Q5: Give one Azure example for each service model.**
IaaS = Azure Virtual Machines, PaaS = Azure App Service, SaaS = Microsoft 365.

**Q6: Which model should a developer choose to deploy a web app without managing servers?**
PaaS — because it handles the OS, runtime, and middleware. The developer only focuses on code.

### Deployment Models
**Q7: What is hybrid cloud? Give an example.**
Hybrid cloud combines public and private cloud. Example: A bank keeps customer data on private cloud but runs its mobile app on public cloud.

**Q8: Which deployment model do startups prefer?**
Public cloud — no upfront cost, easy to scale, fully managed by the provider.

### Virtualization
**Q9: What is a hypervisor?**
Software that creates and manages virtual machines by allocating physical resources (CPU, RAM, storage) to each VM.

**Q10: What is the difference between Type 1 and Type 2 hypervisors?**
Type 1 runs directly on hardware (used in data centers). Type 2 runs on top of an existing OS (used for testing/development).

---

## Homework
- Create a free Azure account at [https://portal.azure.com](https://portal.azure.com)
- Explore the Azure Portal dashboard and note down 5 services you see

---

## Next Class
**Day 2:** Cloud Service Models deep dive and Cloud Deployment Models with real-world scenarios
