# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

I chose to deploy with an App Services for the following reasons:
- We only have lightweight APIs
- Flask is nativly supported by App Services
- App Services is cheaper and scaling is not important for the use case
- The deployment with App Services is easier, faster and azure handles more of the management

| Feature         | Azure App Service                         | Virtual Machines                        |
|-----------------|------------------------------------------|----------------------------------------|
| Costs           | Relatively lower cost, managed platform. Cost depends on the service tier, instances, and usage, and it's generally more cost-effective, especially for smaller workloads | Variable cost, higher responsibility for configuration and management. Cost depends on VM size, OS, and usage (Pay as you go model), and it can be costlier, especially for multiple VM instances   |
| Scalability     | Vertical Scaling only, Vertical scaling without redeployment. Automatically handles load balancing and scaling   | Vertical and horizontal scaling is possible, but manual scaling is required for horizontal scaling  |
| Availability    | High availability and auto scaling      | Depends on manual configuration       |
| Workflow        | Easier deployment and management with less control over configuration        | More involved deployment and management process, more control over configuration and updates         |

### Assess app changes that would change your decision.

I would have taken a VM if
- it would have been a big contract with more hardware power needed
- we have multiple apps, for example for different departments or customer groups (with different programming languages and architectures)
- dedicated servers for security reasons are necessary

There's even a free basic tier for app services, but when you need more compute power, VMs can be cheaper and more flexible:

App Service, 4 cores, 7GB RAM, 10GB Storage = 223,20 $ / Month
VM, 4 cores, 7GB RAM, 120GB Storage = 220,22 $ / Month
