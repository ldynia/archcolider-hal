< [Back](README.md) < [Back to Home](../README.md#solution-structure)

# Data Analytics Platform

## Date

2021-10-30

# Status

Proposed

# Context

FFamily will spend most of its effort in the [Data Analytics Platform](../2.SolutionBackground/data_analytics_platform.md). This is where insights are generated and shared with FFamily customers and collaborators. It's important to keep expenses low:

  - reduce maintainability costs
  - reduce hardware utilization costs
  - make recruitment and onboarding cheap and easy

Additionally, Amazon is default cloud provider for FF solutions, so we need utilize its services wisely:

  - reduce complexity of the solution
  - being cost aware of services that we will use

# Decision

Where it makes sense we will use serverless services that allows for tight cost control such:

  - AWS Lambda (for data transformation tasks, or data backup)
  - AWS QuickSight (for data visualization and reporting)

However, in places where serverless service will create more complexity, we will choose an alternative none serverless service that reduces complexity instead.

  - Amazon Elastic Compute Cloud (EC2) over AWS Lambda
  - Amazon SNS over Amazon Kinesis

In one word, we will favor low complexity over low expenses due to hidden costs associated with complex solutions.

For data analytics tasks, we will push towards the Python stack because it's a popular programming language in the scientific community which is rich in ML libraries, and it's easy to find developers in this community.

# Consequences

**Positive**: Frugal utilization of compute capabilities with serverless solutions will contribute to cost savings.

**Negative**: Serverless technology is relatively new so, the team has to have a dedicated time to learn it.

< [Back](README.md) < [Back to Home](../README.md#solution-structure)
