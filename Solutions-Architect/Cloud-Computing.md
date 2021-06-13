# Cloud Computing

## Definition

1. On-Demand Self-Services
    - Can provision capabilities without human intervention.
2. Broad Network Access
    - Capabilities are available over the network and accessed through standard
        mechanisms.
3. Resource Pooling
    - There is a sense of location independence, no control or knowledge over
        the exact location of the resources.
    - Resources are pooled to serve multiple consumers using a multi-tenant
        model.
4. Rapid Elasticity
    - Capabilities can be elastically provisioned and released to scale rapidly
        outward and inward with demand.
    - To the consumer, the capabilities available for provisioning often appear
        to be unlimited.
5. Measured Service
    - Resource usage can be monitored, controlled, reported, and billed.


## Public vs Private vs Multi vs Hybrid

### Public

- Available to the public. Use only 1 public cloud.
    - AWS
    - Azure
    - Google

### Multi

- Using multiple vendor clouds.

### Private

- On-premises cloud infrastructure.
    - AWS Outpost
    - Azure Stack
    - Google Anthos

### Hybrid

- Mix of public and private cloud solutions. Generally from the same vendor.
- It is NOT public cloud + legacy on-premises.


## Cloud Service Model

- Infrastructure Stack
    - Necessary virtual and physical components.
- Parts you manage
- Parts the vendor manages
- Unit of Consumption

### Infrastructure as a Service (IaaS)

- Vendor manages the physical components.
- Consume O/S.


### Platform as a Service (PaaS)

- Vendor manages the virtualization and physical components.
- Consume runtime.
- E.g. Heroku.


### Software as a Service (SaaS)

- Vendor manages everything.
- Consume the application.
- E.g. Netflix, Dropbox, Gmail.
