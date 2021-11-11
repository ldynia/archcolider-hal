< [Back](README.md) < [Back to Home](../README.md#solution-structure)

# Functional Requirements

A functional requirement is applicable to a software system or its components. It's a description of the service that the software **must offer**. For example, it can be a calculation, data manipulation, business process, user interaction, or any other function specific to business.

# BUSINESS GOAL

Goal of Farmacy Family is to **gather**, **connect**, **communicate** with users and **analyze data** about them. In essence to create a social network around healthy food and community.

# Requirements

- Convert transactional customers to engaged customers.
- Develop relationships between engaged customers and nurture them.
- Provide resources, classes, workshops, videos, recipes, advices, or referrals to dietitians.
- Generate analytical data from medical information to demonstrate the benefits of Farmacy Foods.
- Create deeper engaged by getting intel about: distribution of food, supply and inventory, gluten intolerant, lactose intolerant etc..
- when a transactional customer purchases a meal, Farmacy Family will generate an email elucidating additional benefits available for becoming an engaged customer -solicitation
- Add a new system to manage customer profiles,
- Allowing community engagement
- Allow for personalization around preferences and dietary needs
- Support for integration with 3rd party systems e.g clinicians, dietitians
- Support geographical trend analysis to hone Farmacy Family’s ability to optimize the foods delivered to fridges (an additional integration point TO Farmacy Foods)
- Generate analytical data from medical information. Support for data analytics and visualization.
- Support push and pull models for community engagement.
- Farmacy Family will manage forums, emails, and create connections
between similar demographics.
- Farmacy Family needs transactional member information for outreach purposes. The engagement model includes subscriptions towards related publications, forums that user can participate in created around group interest, reference materials (libraries), class (online class) information, and other media  that supports Food-as-medicine.
- eDietian has access customer profile to improve advice and monitoring of customers. Additionally, the customer and dietitian can interact via messages.
- Allow user to decide what data about him/her should be shared.
- Farmacy Family will include medical profile information and the ability to share information with medical service providers.
- Farmacy Family customers can customize how much profile information they want to allow the community to see, at a fine-grained level.
- Farmacy Family has relationships with third party providers (clinics, doctors, etc) that have access to more analytical data to improve engagement (for example, regional dietary observations).
- Add Farmacy Family user interface to existing Foods interface, which is currently a Reactive monolith.
- Create a holistic UX for both food and Farmacy Family to support engagement model.
- Customer and eDietitian can interact via messages.

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
    - Individual community that interacts with dietician -more personal responses. Multiple integration point per community
  - Clinics
    - Clinic share info to FFood & FFamily if engaged customers allows it!
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