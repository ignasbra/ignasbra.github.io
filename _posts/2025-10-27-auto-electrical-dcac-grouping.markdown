---
layout: post
title:  "Auto device generation based on DC/AC tolerance grouping"
date:   2025-09-26 16:11:09 +0300
categories: Frame grouping
---

**Result**: TBD

**Involvement**: I was the technical owner of the feature. I manged stakeholders
and their requirements and distributed work among developers and QA. I've also implemented a part of the feature.

This feature was our next big milestone in solar park design automation. We had almost automatic electrical generation:
auto stringing, auto device generation and auto cabling.
But each part had to be done separately and a lot of decisions had to be made by the user to glue it all together.

The feature:
* Does stringing automatically.
* It places powerstations based on centers of mass of devices belonging to them.
* It doesn't rely on flat strings per device input, instead it groups devices based on multiple criteria like a DC/AC ratio range,
  azimuth, corridors, shapes of the selected areas, frame capacity, AC power of transformers or central inverters.

<video width="100%" preload="metadata" muted controls loop>
    <source src="/assets/acdc_devices.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>