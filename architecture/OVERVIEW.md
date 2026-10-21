# Conceptual architecture

```mermaid
flowchart TD
Owner[Business owner] --> Workspace[Web workspace]
Workspace --> Workflow[Invoice and acceptance workflow]
Workflow --> Policy[Owner approval and policy controls]
Policy --> Mail[Authorized email integration]
Mail --> Reply[Customer response]
Reply --> Review[Exception review]
Review --> Policy
Workflow --> History[Activity history]
Accounting[Optional accounting integration] --> Workflow
Scheduler[Scheduler when enabled] --> Policy
```

This is a deliberately high-level design, **not a validated production topology**. It intentionally excludes database schema, endpoints, security implementation, credentials, and proprietary agent prompts.
