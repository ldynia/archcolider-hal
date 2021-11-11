< [Back](README.md) < [Back to Home](../README.md#solution-structure)

# Health status sharing with doctors has limited lifespan

## Date

2021-10-30

## Status

Accepted

## Context

Users should be able to share their health status and health records with practitioners (clinics, dietitians). But we can't guarantee that at the time of sharing there will be an integration channel with a system that practitioners use.

Reading information from the phone is not convenient. Besides, clinician  probably would like to copy some data and save a great amount of time instead of retyping what is already in digital format. There should be a way how to share information in easy way.

## Discussion

A user would like to share data about medical records, but bringing everything on papers is not convenient. Usually it's not an option to leave those papers to a practitioner. Also, user can't share data if the clinician is not in the FFamily system. Even so, user would like to select what should be shared and from what period of time.

There are a few options in mind:

- generate QR code - but having data on doctor's phone not the same as have it on PC with patient tracking system
- provide a link by email, sms to a page with medical data - seems to be more convenient as we expect that every practitioner has a working email that is safe to share.

Then the user would like to be sure that shared data can't be used by not authorised persons. It means, that shared link should lead to a static page, with shared information and the link should expire after some time provided by user or FFamily default value (i.e. 0,5-72 hours). It gives confidence that from the link non-shared data might be accessed by program mistake (to some extent) or that the link can be used some time after to get unauthorised access.

## Decision

Create a static page with limited lifespan that provides health status information based on selected settings by the user. Information for sharing should be selected every time when the user would like to create such a page.

## Consequence

- Limits blast radius if a link is high-jacked.
- Sharing the link connected with the user's consent to share data protects FFamily from possible sues.
- Increase amount of work and solutions complexity, but ease data management

< [Back](README.md) < [Back to Home](../README.md#solution-structure)