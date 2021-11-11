< [Back](README.md) < [Back to Home](../README.md#solution-structure)

# System Overview

Short prose description of the system’s function, its users, and any important background or constraints. The purpose is to provide readers with a consistent mental model of the system and its purpose. The system overview is not part of the architecture. However, it is indispensable for understanding the architecture.

## External Systems

1. Clinics - Extranet 3rd party system that shares info to FFood & FFamily only if engaged customers allows for that.
1. Dietician - Extranet 3rd party system design for dieticians to create personal responses with a user or individual communities. System has multiple integration points per community.

## Internal systems

1. Farmacy Foods - Intranet system that allows to create menus in collaborations with medical workers and dieticians.

## System features and responsibilities

The system should allow business to build communities around FFood users and engage with them. Software should allow business to gather data about users, build,  probe and create engagement programs. It means that the main feature of the whole application is to gather and analyze data about users and their behaviour.  Moreover, interactions with 3rd party systems should be logged and extracted data from those systems should be analyzed. The FFamily system should be extensible & modifiable.

### Technical capabilities

1. Collect and store users activity within community
1. Collect and track users geolocation
1. Low delay, spatial notifications based on user location and community events
1. Integration endpoint with clinics and dietitians
1. Process users data and provide access to anonymized health data for researches with ability to filter focus groups by offered criterias
1. HIPAA compliant medical data processing techniques
1. Provide intels to FFood researches to improve variety of meal offers and marketing campaigns

### Users

1. Self-organization communities with information share ability
1. Access to selected educational materials
1. Provide information about health state and meal habits

## Out of scope

1. Create from the ground any sort of media storage\share platform
1. Create from the ground any sort of rich communication platform
1. Seems that [req#11](significant_driving_requirements.md#requirements) is extension and modification of the FFood system only and touches the delivery pipeline that is out of scope.

< [Back](README.md) < [Back to Home](../README.md#solution-structure)