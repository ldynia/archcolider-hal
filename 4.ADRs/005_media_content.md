< [Back](README.md) < [Back to Home](../README.md#solution-structure)

# Keep heavy media materials on public services

## Date

2021-10-30

## Status

Accepted

## Context

One of requirements is to provide access to a media library with educational materials like video, audio, images, text. Users should have a familiar look and feel to control playback, moving to the next image, or read text in a comfortable way.

The media library is controlled by FFamily stuff and users can only consume data. All materials, except video can be rather easily stored using the company cloud storage plan, but video is a very heavy media type and there are a lot of nuances in the video delivery process - graceful degradation, subtitles, playback functionality, encoding and picking up preferable resolution.

## Decision

Keep videos on youtube or similar service. Links to materials should be private and not discoverable by search engines. Main entry point to get info should be the FFamily app.

## Consequences

- Save a lot of time and money developing in-house systems for video uploading, storing, and playback.
- Dependency on 3rd party video service, but if it's big and public then risks of getting it offline is small.


## Risks
- Link to video can be extracted, but video by itself is not a source of monetization, so it's ok. Watermarks of FFamily still will help to inform transactional customers, or unaware people about FFood.

< [Back](README.md) < [Back to Home](../README.md#solution-structure)