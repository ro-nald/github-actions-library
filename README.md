# GitHub Actions Library

A centralized Internal Developer Platform (IDP) asset library. Provides reusable GitHub Actions and workflows designed to standardize CI/CD across an organization, implementing 'Golden Path' patterns for security, scalability, and developer self-service.

```mermaid
graph TD
    subgraph "Dev Team Repos"
        AppA[Frontend App] -- "uses" --> CI
        AppB[Backend API] -- "uses" --> CI
    end

    subgraph "IDP: github-actions-library"
        CI[Standard CI Workflow]
        CD[Deployment Workflow]
        Comp[Setup Composite Action]
        
        CI --> Comp
        CD --> Comp
    end

    style CI fill:#f9f,stroke:#333,stroke-width:2px
    style AppA fill:#bbf,stroke:#333
```

## Upcoming Features

- [ ] Pipeline template to provision EC2 instance for Python application which encrypts traffic up to an ALB (Application Load Balancer)
- [ ] Provide examples on how to consume library templates
- [ ] Enable usage of Terraform Modules library