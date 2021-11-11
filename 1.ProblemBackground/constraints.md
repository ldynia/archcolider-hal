< [Back](README.md) < [Back to Home](../README.md#solution-structure)

# Constraints

Business and technical constraints that impact architecture design. Below lists contain global constraints that drive all trade-off decisions for designed solutions.

## Business

1. Farmacy Food operates in Detroit, one of the poorest cities in [the poorest city in the USA](https://worldpopulationreview.com/us-city-rankings/poorest-cities-in-america).
1. Target group consist mostly of low-income residents, elderly people, college students, educators, senior citizens, and veterans
1. Not much financial support could be provided to communities. They must be self-sustainable in general.

## Technical

1. Budget is limited, so Open-Source software and tools provided by the target platform should end up higher in prioritization.
1. Development team is limited, so the solution should be simple at the beginning to prove business ideas.
1. Time-to-market is critical, and with support of the previous constraint, it should be super simple to deploy.
1. AWS is the primary target platform for deployment.

# Risks

## Business

1. Market of medical data management needs to be analysed for the Detroit area. Disclosing this data with 3rd parties might be difficult.
1. Convince medical 3rd parties (clinics, practitioners) that medical data will be secured and used for a good will that follows complaints.
1. Users consent to collect and share medical data.
1. Convince local shops to provide targeted ad campaigns for communities, or provide information about discounts. There should be an easy way to create comparings or integrate existing systems with FFamily.
1. Why should users communicate in FFamily application? Existing channels such Facebook, and What's App can be utilized instead.

## Technical

1. Probably there is no dedicated data scheme to onboard clinics. There are no organizations with rich technical support. Most clinics probably are using some standard software approved by the clinics association or so. API is questionable and read\write data is  a big concern. The number of different integrations might be overwhelming.
1. No good open-source solutions for features needed by FFamily

< [Back](README.md) < [Back to Home](../README.md#solution-structure)