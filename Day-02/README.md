# Day 2 - Cloud Service Models & Deployment Models Deep Dive

## Learning Objectives
- Understand IaaS, PaaS, SaaS in depth with real-world scenarios
- Learn how to choose the right service model for a given problem
- Understand deployment models with Indian industry examples
- Learn about Multi-Cloud and Community Cloud

---

## Quick Recap of Day 1
- Cloud Computing = renting IT resources over the internet, pay-as-you-go
- 5 Characteristics: On-demand, Broad access, Resource pooling, Elasticity, Measured service
- Virtualization = running multiple VMs on one physical server using a Hypervisor

---

## 1. IaaS - Infrastructure as a Service (Deep Dive)

### What You Get
The cloud provider gives you raw infrastructure — virtual machines, storage, and networking. You manage everything from the OS upward.

### Real-World Scenario
> Your company has an old Java application running on Windows Server 2012. Management wants to move it to cloud WITHOUT changing the code. You need the exact same OS and configuration.
> **Solution:** Create an Azure VM with Windows Server 2012, install Java, deploy your app. This is IaaS.

### When to Choose IaaS
- You need full control over the operating system
- Migrating legacy applications that can't be modernized
- Custom security or compliance configurations needed
- Running software that requires specific OS-level settings
- Need root/admin access to the server

### Azure IaaS Services
| Service | Purpose |
|---|---|
| Azure Virtual Machines | General-purpose compute |
| Azure Virtual Network | Custom networking |
| Azure Disk Storage | Persistent storage for VMs |
| Azure Load Balancer | Distribute traffic across VMs |

### Pros & Cons
| Pros | Cons |
|---|---|
| Full control over infrastructure | You manage OS patches & updates |
| Custom configurations possible | Requires sysadmin skills |
| Run any software you want | More responsibility = more work |
| Best for legacy migrations | Scaling requires manual setup |

---

## 2. PaaS - Platform as a Service (Deep Dive)

### What You Get
The cloud provider manages everything except your application code and data. You just write code and deploy.

### Real-World Scenario
> A startup wants to build a food delivery app backend using Python Flask. They have 3 developers and zero IT staff. They don't want to worry about servers, OS, or scaling.
> **Solution:** Use Azure App Service. Push code via `git push`, and Azure handles server, OS, runtime, scaling, and SSL certificates. This is PaaS.

### When to Choose PaaS
- Building new web applications or APIs
- You want to focus only on code, not infrastructure
- Need automatic scaling without manual setup
- Building microservices architecture
- Mobile app backends

### Azure PaaS Services
| Service | Purpose |
|---|---|
| Azure App Service | Web apps and APIs |
| Azure SQL Database | Managed database |
| Azure Functions | Serverless code execution |
| Azure Cosmos DB | Globally distributed database |
| Azure DevOps | CI/CD and project management |

### Pros & Cons
| Pros | Cons |
|---|---|
| No server management | Less control over environment |
| Auto-scaling built in | Vendor lock-in risk |
| Faster time to market | Limited OS-level access |
| Built-in CI/CD support | May not support all languages |

---

## 3. SaaS - Software as a Service (Deep Dive)

### What You Get
Fully managed software delivered over the internet. You just open a browser and use it. Zero technical setup.

### Real-World Scenario
> TCS has 500,000 employees who need email, video calls, and file sharing. They don't want to set up email servers across 46 countries.
> **Solution:** Subscribe to Microsoft 365. Employees log in from any device, anywhere. IT team manages user accounts, not servers. This is SaaS.

### When to Choose SaaS
- Standard business applications (email, CRM, HR, accounting)
- No technical team available
- Need quick deployment across many users
- Want zero maintenance responsibility

### Popular SaaS Examples
| Software | Category |
|---|---|
| Microsoft 365 | Productivity (Email, Docs, Teams) |
| Salesforce | CRM |
| Slack | Communication |
| Zoom | Video Conferencing |
| GitHub | Code Repository |
| Jira | Project Management |

### Pros & Cons
| Pros | Cons |
|---|---|
| Zero setup or maintenance | Least control |
| Accessible from anywhere | Data is with the provider |
| Automatic updates | Customization is limited |
| Subscription model (affordable) | Internet required always |

---

## 4. How to Choose: Decision Framework
