*DRAFT*

:bangbang: This is FAAAAAARRR from finished :-)

Todo:
1. Finish the document
2. Rename chapter and paragraph when the text is done
3. Split into logical chapters for easy navigation
4. Find a place for it and move it there

# Analytical data
- [ ] Data is either operational or analytical in nature.
- [ ] Distribution for either is different
- [ ] Different needs: Operational, Near-Realtime analytics, Reporting, AI/ML
- [ ] 

## Introduction
This chapter aims to give context to the user both in the use of data terminology but also to ease into the meat of the subject matter (Family Food)

## Ingestion
The concept of ingestion is centered around getting data into your organization. Data can come from many sources and these sources may be found both in- or outside of your organisation. This architecture mostly concerns the following types of sources:

* Open data from the web
* Internal systems data
* External systems data
* User interaction data
* User input data

In general, we strive to uniformly allow for ingestion of data while providing a sensible number of integration patterns.

### Open data from the web
In recent years we have seen an explosion of freely available data being publicly provided through the internet. The broad spectrum of freely available data is mind-blowing.

Do you need to know the population density anywhere in the world? No problem, the UN data is right there for you to grab. See: [UNData](http://data.un.org/)

### Internal systems data
We define internal systems as systems that are in a strong influence sphere of the organisation.

Examples of internal systems:
* On-premise systems
* In-house developed systems
* 

### External systems data
We define external systems as systems that the organisation has very little to no control over.

Examples of external systems:
* [COTS](../glossary.md#Abbreviations) applications
* 

### User interaction data
Any time a user interacts with one of the organisation's systems there is a potential for a meaningful event to occur. For instance, we could identify user interactions when looking at certain pages on the web-site or when abbandoning a shopping cart.

### User input data
User input is data provided by the user in a conscious effort to send data to the organisation. This could, for instance, be input from a form on the website.

### Meta-data

### Data lineage
We define data lineage as a route data takes throughout the company and possibly beyond. This includes the starting point of a dataset and the location(s) it travelled  through to reach the target systems. The target system is also part of the data's lineage.

In most systems we also include the reason that data was moved to a certain spot on the route. Let's make that a bit more visual:

TODO: Add figure to explain data lineage.

### Data provenance 
TODO: Possibly skip this paragraph and roll it into data lineage in the interest of time and as not to confuse the reader too much.

### Golden source
The orginal source of a data set. This concept functions both as a boundary for data lineage and (to some extent) defines the boundaries for quality assurance of the data.

- [ ] Write on the avoidance of circular patterns

Data gets aggregated 

### Golden dataset
- [ ] May not be needed in this kata's discussion.

## Storage
- [ ] How to store data for certain targets

## Modeling
- [ ] Modeling data for elasticity demands without going full ham

## Governance
Data governance is the process of managing the availability, usability, integrity and security of the data in enterprise systems, based on internal data standards and policies that also control data usage. Effective data governance ensures that data is consistent and trustworthy and doesn't get misused. It's increasingly critical as organizations face new data privacy regulations and rely more and more on data analytics to help optimize operations and drive business decision-making.

## Security
Though part of data governance we consider security such a paramount concept that we want to discuss it explicitly in this architecture. Though everybody has some notion of what data security looks like the nuances are quite important especially when handling privacy-sensitive information. 

## Distribution
When data resides in one systems and is needed by another we need some kind of mechanism that can get it from the source to the target system. How we distribute data within our organisation is an important consideration.

Consider a system that needs near-realtime data in order to function properly but the available data distribution mechanism only support an eventual reply to a request.

## Data Delivery Agreements
A data delivery contract is a formal agreement that provides assurances from the data provider to the data consumer and vice versa. The data provider states that they will deliver the data and how the consumer can ingest the data. 

The agreement defines the interface of both the data and the delivery/retrieval mechanisms available. Any Service Level Agreement is also considered to be part of the Data Delivery Agreement.

Any Data Delivery Agremeement should contain a formalized definition of how the consumer can use the data that the provider provides. For example, some data is very fresh and of an exploratory nature. This may lead to a DDA that specifies that you may use the data but that production use is protected by disclaimer that states that the provider takes no responsibility for its correctness.

## Data Sharing Agreements
Data sharing agreements are all about how the consumer is allowed to use the data. For example, any user e-mails received by the consuming system may remain in there data store no longer than 1 business day.

DSAs are not technical in nature but define the rules and processes needed in order to properly use the data. The burden is therefore mostly on the consuming side to provide their intended use. For the purpose of this architecture we specifically stipulate that no data may be forwarded without explicit permission. These permissions should lead to an ADR since they are considered to be a deviating from the desired state architecture.

## Historical data


## 
