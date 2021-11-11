< [Back](README.md) < [Back to Home](../README.md#solution-structure)

# Use external webinar platform without deep integration into FFamily

## Data

2021-10-31

## Status

Accepted

## Context

The FFamily system's intention is to provide access to live consultations with practitioners (doctors, dietitians). Also, there is a requirement to support community events, online and offline.

## Discussion

Webinars is not a core subdomain for FFamily and it's a highly generic solution. For the first iteration there is no need for deep integration of webinars into the system, as communities most of the time, by definition, could meet face to face and discuss their needs. It means that webinars are required for global community events and consultancy services. For those activities FFamily admins could create sessions on-demand in case of events. And schedule repeated sessions for consultancy needs. Or there might be a pool of predefined links for online sessions.

Another possibility is to use WebRTC, it's open standard and there are a lot of examples on how to organize p2p connections. There are many nuances if one wants to create a big web conference, but for p2p communication it should be ok. However implementation requires time, but using external platforms gives us speed to offer features sooner. Later we can review this approach if it shows potential and there would be public demand. For now we follow [architecture principles](../2.SolutionBackground/solution_overview.md#principles)

## Decision

Use external public webinar platforms like Zoom, BlueJeans, GoToMeeting, YouTube Live, Google Hangout depends on event type and required capabilities.

For instance:
- Youtube live - when active participation is not assumed. Comments allowed.
- Zoom - for smaller or individual meetings.

## Consequences

- Connection process might be unfamiliar for participants. Application should explain and guide what to do.
- Usage of 3rd party services reduce possibilities for branding and adding features.
- Gives us chance to gradually migrate to WebRTC solution when we will be ready

< [Back](README.md) < [Back to Home](../README.md#solution-structure)