< [Back](README.md) < [Back to Home](../README.md#solution-structure)

# Business Drivers

## Business goal:

*Farmacy Food's goal is to work with you to recognize that achieving your health goals can be done with convenience. Farmacy Family is an enhancement of the Farmacy Foods system. Goal of Farmacy Family is to connect and gather users, analyze data about them, and communicate with them. In essence to create a social network around healthy food and community.*

### Primary goals (provided):
1. Convert transactional customers to engaged customers.
   - Develop relationships between engaged customers and nurture them.
2. Provide resources, classes, workshops, videos, recipes, advice, or referrals to dietitians.
3. Generate analytical data from medical information to demonstrate the benefits of Farmacy Foods.
   - Create deeper engagement by getting intel about: distribution of food, supply and inventory, gluten intolerant, lactose intolerant etc..

When a transactional customer purchases a meal, Farmacy Family will generate an email elucidating additional benefits available for becoming an engaged customer -solicitation

In essence, the business goal is to:
- Improve market position.

Thinking about data analysis and insights that it can provide for marketing, and additional monetization channels, there is:
- Improve confidence in and perception of the system.

## Business Drivers (BD)

1. Increase users' awareness about FFood products and engage them to buy more food from the FFood system.
1. Gather information about the relationship between user health conditions and a diet and produce intel data for marketing and research.
1. Improved use of analytics driven through the new integration of Farmacy Family will help gather new investors and prove better dietary outcomes in member communities
1. System provides recommendations based on user data about consumed meals
1. System should be easy to use for inexperienced users to increase the user base.
1. Involve other specialists in health areas to increase user base, and provide a basement for possible research.
1. Provide tools to organize self-sustainable communities, where members can support each other by various activities

# Significant Architectural Requirements (SAR)

List of architecture driving requirements (primary functional, quality attribute, and life-cycle requirements)

| # | Significant Architectural Requirements | From BD |
|----|----|----|
| 1 | User's location tracking to maximize involvement and awareness providing the most relevant offers | 1, 6 |
| 2 | Personal and medical data protection, regulation compliance | 2, 5 |
| 3 | Keep cause-effect information for analytical and marketing capabilities | 1, 2, 3, 5, 6 |
| 4 | Extensibility of the system with new community support tools | 6, 3, 5, 1 |
| 5 | Cross-system integration (FFood, FFamily) of UX and targeted marketing campaign  | 1, 6 |
| 6 | Food recommendations knowledge base  | 3, 5, 6 |
| 7 | Integration points ready for customization on demand when connect clinics, dietitians | 5, 2 |
| 8 | Fine-grained access to analytical data for researches | 2, 3, 5 |
| 9 | Reporting and notification tools for community members | 1, 6, 2, 3 |

## Requirements

The list below is provided by FFood

| # | Requirement | SAR | Quality Attributes |
|---|---|---|---|
| 1 | Convert transactional customers to engaged customers | Non technical problem | |
| 2 | Develop relationships between engaged customers. Some engagement platform is needed **buy vs build**. | 4 | Extensibility, Interoperability |
| 3 | Add a new system to manage customer profiles, allowing community engagement, and personalization around preferences and dietary needs | 2, 5 | Modifiability, Security |
| 4 | Support for integration with 3rd party systems e.g clinicians, dietitians | 7, 8 | Interoperability, Extensibility |
| 5 | Support geographical trend analysis to hone Farmacy Family’s ability to optimize the foods delivered to fridges (an additional integration point TO Farmacy Foods). _Seems to be out of scope_ | 1 |  |
| 6 | Generate analytical data from medical information. Support for data analytics and visualization. | 1, 3, 8, 9 | Interoperability |
| 7 | When a transactional customer purchases a meal, Farmacy Family will generate an email elucidating additional benefits available for becoming an engaged customer. | 3, 5 | Observability |
| 8 | Support push and pull models for community engagement. In other words, Farmacy Family will manage forums, emails, and create connections between similar demographics. | 4 | Observability |
| 9 | Farmacy Family needs transactional member information for outreach purposes. The engagement model includes subscriptions towards related publications, forums that users can participate in created around group interest, reference materials (libraries), class (online class) information, and other media  that supports Food-as-medicine. | 4 | - |
| 10 | eDietian has access to customer profile to improve advice and monitoring of customers. Additionally, the customer and dietitian can interact via messages. | 7 | UX, Security |
| 11 | Farmacy Family wants to improve the distribution and potential food waste by preventing the wrong mix of foods in a particular fridge.. _Seems to be out of scope_ | 3 | - |
| 12 | Farmacy Family will include medical profile information and the ability to share information with medical service providers. | 8 | Security, UX |
| 13 | Farmacy Family customers can customize how much profile information they want to allow the community to see, at a fine-grained level. | 2 | Security |
| 14 | Farmacy Family has relationships with third party providers (clinics, doctors, etc) that have access to more analytical data to improve engagement (for example, regional dietary observations). | 7, 8 | Interoperability |
| 15 | Add Farmacy Family user interface to existing Foods interface, which is currently a Reactive monolith. Create a holistic UX for both food and Farmacy Family to support engagement models. | 5 | UX |
| 16 | Customer and eDietitian can interact via messages. | 7, 9, 4 | Usability, Security |

Requirements #5 and #11 belongs to FFood domain and does not fit the declared business goal.

# Technical Details

## Domain areas

- Onboarding new engaged customers
  - profile for customer (username & password) we need rich profile metadata!
  - analytics
- Community
  - forum (localized -geographical, temporal -materials age out!)
  - in person / virtual events (localized, temporal)
  - classes (localized, temporal)
  - interactive media library (global -all FFamily users, reference)
  - general wellness education (global, reference)
- Integration with 3rd parties (extranet)
  - Dietician
    - Individual community that interacts with dietitian -more personal responses. Multiple integration point per community
  - Clinics
    - Clinic shares info to FFood & FFamily if an engaged customer allows for it!
  - Farmacy Foods (existing system) To create menus in collaborations with medical worker and dietician
    - Intranet integration to convert transactional customers to engaged customers

## Engagement Models

- Clients
  - Covered above - building a community, education, increased awareness
- Clinics - Work with clinics to establish baseline tests for clients
  - Gather results
  - Test every 3 months
  - Analyze results
  - Demonstrate any change in their overall health
  - Use this info to gain investors and additional support and help
- Dieticians
  - Regular contact via messages
  - Selective access to medical information about the customer from a partner clinic (Integration)
  - Farmacy Foods supported generic advice from dieticians. Farmacy Family will support one-on-one advice for engaged customers
- Farmacy Family
  - Farmacy Foods needs to know which transactional customers are Engaged Customers.
  - Farmacy Food needs to know which Transactional Customers (and their information) are not part of Farmacy Family (Engaged Customer) to start the onboarding process for those customers. (Integration of two systems).

# Additional Context

- The new system must seamlessly incorporate into Farmacy Foods
- Improved use of analytics driven through the new integration of Farmacy Family will help gather new investors and prove better dietary outcomes in member communities

## Resources

- https://www.semha.org/
- https://www.farmacyfood.com/

< [Back](README.md) < [Back to Home](../README.md#solution-structure)