# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

I chose to deploy with an App Services for the following reasons:
- We only have lightweight APIs
- Flask is nativly supported by App Services
- App Services is cheaper and scaling is not important for the use case
- The deployment with App Services is easier, faster and azure handles more of the management

### Assess app changes that would change your decision.

I would have taken a VM if
- it would have been a big contract with more hardware power needed
- we have multiple apps, for example for different departments or customer groups (with different programming languages and architectures)
- dedicated servers for security reasons are necessary