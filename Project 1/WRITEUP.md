# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

VM: 
- Higher costs in terms of labor/time -> it includes that you have to take care on the OS set up as well which can be more time consuming compared to App Service.
- Scalability is very high, flexible types/sizes possible, load balancing options with multiple VMs in a group
- Availability is very high, full access to OS
- Workflow: Custom images can be rolled out very easily

App Service:
- Costs based on the App Service Plan - for the CMS very low costs in a basic plan; No OS set up needed
- Very high, auto-scaling but limited resources for big software projects
- Availability is very high, based on your App Service Plan
- Continuous Deployment via Github


-> Choice: App Service
Focussed only on the application itself. No need for a different option besides PaaS.
Our application is very simple and doesn't require high performance or much resources.
Deployment via Github, no need to access OS level



### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

- I need access to the OS (or I want full control) because of the size of the project, or for deployment purposes
- I need very high performance in terms of CPU or storage which would exceed the limits of App Services
- I need horizontal scalability in a group of VMs to increase availability and to do load balancing
- I offer a service for a CMS for other people and it's rolled out via an custom image to create a new instance for every customer