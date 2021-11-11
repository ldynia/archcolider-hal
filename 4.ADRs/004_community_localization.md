< [Back](README.md) < [Back to Home](../README.md#solution-structure)

# Access to communities based on user's main localization

## Dates

2021-10-21

## Status

Proposed

## Context

FFamily would like to organize communities for neighborhoods to help them develop healthy eating habits and support specific social groups. There should be a way to point user to the community that fits best and allows the user to participate in local activities. Locality also means higher trust between members. They have more common interests and probably have the same problems to overcome.

## Discussion

It would be not wise to create all communities globally available for everyone. FFamily is not a social network in traditional meaning and it should connect people who live in a compact area. It means, there is no sense to provide a full list of communities for everyone.

Free access to all communities won't help build trust within them, as we see it. Members of the community should have some confidence that a new member would contribute to community activity, because everyone would like to live in a better neighborhood.

However, user's address does not restrict participation in any events organized by communities if the user is nearby.

## Decision

User should provide main living area and based on this information the system will suggest communities to join.

However, user's address do not restrict participate in any events organized by communities if the user nearby.

## Consequences

- Local affinity of data provides a certain level of confidence that data about community activity don't need to be sophisticatedly synchronized between servers.
- Possible decisions to deploy and control resources required for processing community data are predictable.
- This limitation also helps build boundaries of data clusters for further analysis.
- Global groups is special case and requires additional modeling

< [Back](README.md) < [Back to Home](../README.md#solution-structure)
