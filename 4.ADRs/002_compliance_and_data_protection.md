< [Back](README.md) < [Back to Home](../README.md#solution-structure)

# Compliance & Data Protection

## Date

2021-10-29

## Status

Proposed

## Context

The core domain of FFamily is data analytics for health benefits and wellness of its customers. To do so FFamily will integrate with clinicians (3rd party systems).

Client's personal data integrated with clinicians data will fall into the category of medical data and will be affected by the [Health Insurance Portability and Accountability Act](https://en.wikipedia.org/wiki/Health_Insurance_Portability_and_Accountability_Act) known as HIPAA - that talks about data protection from fraud and theft (among others)

Additionally, because of integration with 3rd parties systems we need to ensure data security in transit and rest.

## Decision

We will utilize [Amazon Inspector](https://aws.amazon.com/inspector/) - an automated security assessment service that helps improve the security and compliance of applications deployed on AWS.

Furthermore, we will utilize [Amazon EC2 Systems Manager](https://aws.amazon.com/systems-manager/) - a unified user interface, so you can track and resolve operational issues across your AWS applications and resources from a central place.

We will strive to use the [AES-256](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) encryption algorithm (the strongest encryption algorithm at the moment) for data encryption at rest and on transit.

## Consequences

Data is encrypted, and Amazon services that we are utilizing now are HIPAA eligible.

**Positive:** Increased data security, and compliance with HIPAA achieved.

< [Back](README.md) < [Back to Home](../README.md#solution-structure)
