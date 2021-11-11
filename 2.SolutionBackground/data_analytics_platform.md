< [Back](README.md) < [Back to Home](../README.md#solution-structure)

# Data Analytics Platform

This section proposes architecture for data and analytics activities of FFamily business.

# Data Platform Architecture

The below diagram illustrates the architecture of **Data Analytics Platform**. The diagram has been designed with the ELT (Extract, Load, Transform) process in mind. The ELT process starts in the first box from the left and ends in the last box on the right.

<div align="center">

| <img src="../docs/img/idap.png" width="800"> |
| :---: |
| **Data Platform Architecture** |

</div>

Architecture of Data Analytics Platform shows areas of responsibilities:

- Data Creation - area where external and internal data is extracted from.
- Data Ingestion - area that fetches and transforms data.
- Persistent Storage - a data lake holding data being ready for analysis.
- Data Analytics - a data mining area, here information is inferred from data residing on persistent storage.
- Data Visualization and Reporting - area that transfers information into comprehensive and appealing form.
- Infrastructure Platform - a platform supporting all above activities.

# Data Platform Team

It's hard to talk about organizational topology when we are dealing with a small startup. Yet, Conway's law applies to every organization independently of its size. The Conway's law states that:

> Any organization that designs a system will produce a design whose structure is a copy of the organization's communication structure. - Malvin E. Conaway

FFamily solution is an extension to FFood system - which is implemented as a modularized monolith. FFamily solution will naturally lean towards it.

It's important to mention areas of responsibilities within the Data Analytics Platform. We can distinguish several roles that are needed to sustain FFamily data platform: Developer, Cloud Engineer,  Data Engineer and Data Analyst. Because there is an overlap between skills of Developer, Data Engineer and Data Analyst, we are proposing to unify these three jobs into a role of Data Scientist.

<div align="center">

| <img src="../docs/img/data_scientist.jpg" width="400"> |
| :---: |
| Data Scientist |

</div>

Data Analytics Platform **Core Team** is illustrated in the image below.

<div align="center">

| <img src="../docs/img/trinity.jpg" width="400"> |
| :---: |
| **Core Team** |

</div>

# Data Platform Services

Because Amazon is the default cloud provider for FFamily, we'll utilize appropriate Amazon services applicable for every area in the Data Analytics Platform.

<div align="center">

| <img src="../docs/img/idap_aws.png" width="800"> |
| :---: |
| **Data Platform Architecture** |

</div>

Every area in Data Analytics Platform has a role that is specialized in that area. The reality is that responsibilities in a role can be shared between different members of a core team.

| | Area | Role |
| -- | --- | --- |
| <img src="../docs/img/icons/file.png" width="50"> | Data Creation | Developer |
| <img src="../docs/img/icons/file_cabinet.png" width="50"> | Data Ingestion | Data Scientist / Developer |
| <img src="../docs/img/icons/analytics.png" width="50"> | Data Analytics | Data Scientist / Developer |
| <img src="../docs/img/icons/report.png" width="50"> | Reporting & Visualization | Data Scientist |
| <img src="../docs/img/icons/infra.png" width="50"> | Infrastructure Platform | Cloud Engineer |
| | | |

# AWS Services Explained

| | Service | Purpose |
| :---: | --- | --- |
| <img src="../docs/img/icons/aws-dynamodb.png" width="50"> | DynamoDB | Managed NoSQL database  |
| <img src="../docs/img/icons/aws-sns.jpeg" width="50"> | Simple Notification | Messaging service |
| <img src="../docs/img/icons/aws-lambda.png" width="50"> | Lambda | Event-driven serverless computing platform |
| <img src="../docs/img/icons/aws-quick-sight.png" width="50"> | QuickSight | Tool for data visualization |
| <img src="../docs/img/icons/aws-sage-maker.jpg" width="50"> | SageMaker | Machine-Learning platform |
| <img src="../docs/img/icons/aws-iam.png" width="50"> | IAM | User Access Management |

< [Back](README.md) < [Back to Home](../README.md#solution-structure)