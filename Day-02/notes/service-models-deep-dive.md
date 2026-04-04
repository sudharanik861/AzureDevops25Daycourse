# Cloud Service Models - Detailed Notes

## The Shared Responsibility Model

Cloud computing is about dividing responsibility between YOU and the PROVIDER.
The more responsibility the provider takes, the less control you have — and vice versa.

### Responsibility Layers (Bottom to Top)
1. Networking
2. Storage
3. Servers (Physical)
4. Virtualization
5. Operating System
6. Middleware
7. Runtime
8. Application
9. Data

---

## IaaS - Infrastructure as a Service

### Definition
Provider gives you virtualized hardware (VMs, storage, networking).
You install and manage everything from the OS upward.

### How It Works
1. You go to Azure Portal → Create Virtual Machine
2. You choose: OS (Windows/Linux), VM size (CPU, RAM), Disk, Network
3. Azure provisions the VM in minutes
4. You SSH/RDP into the VM
5. You install your software, configure security, manage patches

### Azure IaaS Services
- **Azure Virtual Machines** — General purpose compute
- **Azure Virtual Network (VNet)** — Custom networking and subnets
- **Azure Disk Storage** — Persistent disks for VMs
- **Azure Load Balancer** — Distribute traffic across VMs
- **Azure Virtual Machine Scale Sets** — Auto-scale VMs based on demand

### Pricing Model
- Pay per **VM per hour**
- Cost depends on: VM size, OS license, disk type, region
- Example: Standard B1s VM (1 vCPU, 1 GB RAM) ≈ ₹6-8/hour

### Real-World Use Cases
| Company | Use Case | Why IaaS? |
|---|---|---|
| Banks | Legacy core banking on Windows Server | Need exact same OS configuration |
| Gaming | Custom game servers with specific GPU | Need GPU access and low-level control |
| Research | HPC (High Performance Computing) clusters | Need custom Linux kernels |
| Migration | Lift-and-shift of on-prem apps | Fastest path to cloud with no code changes |

---

## PaaS - Platform as a Service

### Definition
Provider manages infrastructure + OS + runtime.
You only manage your application code and data.

### How It Works
1. You write your application code (Python, Node.js, Java, .NET)
2. You push code to Azure App Service via Git or CI/CD
3. Azure handles: server provisioning, OS patches, runtime updates, SSL, scaling
4. Your app is live with a URL in minutes

### Azure PaaS Services
- **Azure App Service** — Web apps, REST APIs
- **Azure SQL Database** — Managed relational database
- **Azure Cosmos DB** — Globally distributed NoSQL database
- **Azure Functions** — Serverless code execution (pay per execution)
- **Azure Kubernetes Service (AKS)** — Managed Kubernetes
- **Azure DevOps** — CI/CD pipelines and project management

### Pricing Model
- Pay per **app instance** or **per request**
- Azure App Service: Free tier available, then ₹1,000-10,000/month based on plan
- Azure Functions: First 1 million executions FREE per month

### Real-World Use Cases
| Company | Use Case | Why PaaS? |
|---|---|---|
| Startups | New web app with 3-person dev team | No IT staff, need to ship fast |
| E-commerce | Product catalog API | Auto-scaling during sales |
| Mobile apps | Backend API for mobile app | Focus on features, not servers |
| SaaS companies | Multi-tenant application | Built-in scaling and monitoring |

---

## SaaS - Software as a Service

### Definition
Fully managed software delivered over the internet.
You just create an account and start using it.

### How It Works
1. Go to the software's website
2. Sign up / Login
3. Start using immediately
4. No installation, no configuration, no maintenance

### Popular SaaS Products
| Software | Category | Users |
|---|---|---|
| Microsoft 365 | Productivity | 400M+ users |
| Salesforce | CRM | 150K+ companies |
| Slack | Communication | 750K+ organizations |
| Zoom | Video Calls | 300M+ daily users |
| GitHub | Code Repository | 100M+ developers |
| Jira | Project Management | 10M+ users |
| Google Workspace | Productivity | 3B+ users |

### Pricing Model
- Pay per **user per month**
- Microsoft 365 Business: ₹500-1,500/user/month
- Salesforce: ₹1,500-25,000/user/month
- Slack: Free tier, then ₹200-500/user/month

---

## Comparison Summary

| Factor | IaaS | PaaS | SaaS |
|---|---|---|---|
| You manage | OS, Apps, Data | Apps, Data | Nothing |
| Provider manages | Hardware, Network, Virtualization | + OS, Runtime, Middleware | Everything |
| Control | Highest | Medium | Lowest |
| Flexibility | Maximum | Moderate | Minimal |
| Skill needed | Sysadmin + Developer | Developer | End user |
| Deployment time | Days-Weeks | Hours-Days | Minutes |
| Scaling | Manual or scripted | Automatic | Automatic |
| Cost model | Per VM/hour | Per app/request | Per user/month |
| Best for | IT teams, migrations | Developers, startups | Business users |
