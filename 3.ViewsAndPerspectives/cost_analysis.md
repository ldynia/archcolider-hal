< [Back](README.md) < [Back to Home](../README.md#solution-structure)

# Cost Analysis

## Data Analytics Platform

This section contains estimation of services used by [Data Analytics Platform](../2.SolutionBackground/data_analytics_platform.md).

### Amazon Lambda

Below table was created with the [Amazon Lambda calculator](https://s3.amazonaws.com/lambda-tools/pricing-calculator.html). AWS Lambda pricing can be found [here](https://aws.amazon.com/lambda/pricing/).

We are going to utilize Lambda functions in the context of the ELT process (data transformation tasks). Data will be normalized from bronze (raw data), to silver (filtered, cleaned and augmented) to gold (business-level). We expect to run those jobs daily. Because these tasks are nor frequent, we are expecting zero costs for utilization of this service.

**Notes:** For the first 1 million requests lambda is free.

| Task/Context | Requests/month | Duration | Price |  |
| --- | --- | --- | --- | --- |
| Data Extraction | 31 | N seconds | 0 | |
| Data Normalization | 93 = (3 x 31) | N seconds | 0 | |
| Data BackUp | 31 | N seconds | 0 | |
| **Total cost** |  |  | 0 | USD/month |

### Amazon QuickSight

Amazon QuickSight pricing can be found [here](https://aws.amazon.com/quicksight/pricing/).

Dashboards generated with Amazon QuickSight have a fixed price based on business model. Moreover, dashboard reads can be charged as $0.30 USD per session, however the cost will not exceed the fixed threshold set by Amazon which is $5 USD/month.

| Task/Context | USD |
| --- | --- |
| Enterprise Subscription | 24 |
| Readers | 5 |
| **Total cost** | **$29** |

### Amazon SageMaker

To cut costs on the Amazon SageMaker service, we are going to use **On-Demand Notebook Instances** rather than **SageMaker Studio Notebooks**. Below table was created with the [Amazon SageMaker calculator](https://calculator.aws/#/createCalculator/SageMaker).

| Task/Context | USD/month  | USD/month |
| --- | --- | --- |
| Number of data scientist(s) | 1 | 2 |
| Number of On-Demand Notebook instances per data scientist | 8 | 8 |
| On-Demand Notebook hour(s) per day | 6 | 6 |
| On-Demand Notebook day(s) per month | 20 | 20 |
| **Total cost** | **$215** | **$429** |

### Amazon SNS

Below table was created with the Amazon [Amazon SNS calculator](https://calculator.aws/#/createCalculator/SNS).

| Task/Context | USD/month | USD/month |
| --- | --- | --- |
| Requests [million/month] | 1 | 2 |
| SQS Notifications [million/month] | 1 | 2 |
| **Total cost** | **$0** | **$0.50** |

### Amazon Dynamo DB

Below table was created with [the Amazon Dynamo DB  calculator](https://calculator.aws/#/createCalculator/DynamoDB).

| DynamoDB Type | USD/month | USD/month  |
| --- | --- | --- |
| millions reads/month | 1 | 2 |
| millions writes/month | 1 | 2 |
| **Total cost** | **$1.38** | **$2.75** |

### Amazon S3

Below table was created with the [Amazon S3 calculator](https://calculator.aws/#/createCalculator/S3). Additional info [here](https://www.youtube.com/watch?v=JWz4eCczCkQ&t).

| | | USD/month | | USD/month |
| --- | --- | --- | --- | --- |
| **S3 Standard** | |  | | |
| Storage GiB/month | 300 | | 600 | |
| No requests to S3/month | 100000 | | 1000000 | |
| No requests from S3/month | 100000 | | 1000000 | |
| Price/month | | 7.44 | | 19.20 |
| **Data Transfer** | | | | |
| Inbound Data Transfer GiB/month | 100 | | 500 | |
| Outbound Data Transfer GiB/month | 100 | | 500 | |
| Price/month|  | 8.91 | | 44.91 |
| **S3 Glacier** | | | | |
| Storage/month | 100 | | | |
| S3 Glacier Average Object Size MiB | 16 | | 16 | |
| No requests to S3/month | 10000 | | 1000000 | |
| Price/month|  | 0.7 | | 32.01 |
| **Total cost** | | **$17.05** | | **$96.12** |

## Summary of Costs Per Year

Below table shows estimated costs of the [Data Analytics Platform](../2.SolutionBackground/data_analytics_platform.md) implemented in AWS cloud.

**TODO:**
- Estimate cost for other none DAP services such EC2 and COTs What costs???

| Service | TCO at projected growth per year | TCO at rapid growth per  year |
| --- | --- | --- |
| Amazon Lambda | 0 | 0 |
| Amazon QuickSight | 348 | 348 |
| Amazon SageMaker | 2580 | 5148 |
| Amazon SNS | 0 | 6 |
| Amazon Dynamo DB | 16.56 | 33 |
| Amazon S3 | 204.6 | 1153.44 |
| Data Transfer out | TBD | TBD |
| **TOTAL COST** | **$3149.16 USD** | **$6688.44 USD** |

< [Back](README.md) < [Back to Home](../README.md#solution-structure)