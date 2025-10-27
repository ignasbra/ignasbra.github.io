---
layout: post
title:  "Auto device generation based on DC/AC tolerance grouping"
date:   2025-09-26 16:11:09 +0300
categories: Frame grouping
---

**Result**: TBD

**Involvement**: I was the technical owner of the whole feature, one developer assisted with the implementation.

This feature was our next big milestone in solar park design automation. We had almost automatic electrical generation: auto stringing, auto device generation and auto cabling. 
But each part had to be done separately and a lot of decisions had to be made by the user to glue it all together.
An unsuccessful attempt was made some time ago that made a lot of assumptions about where powerstations should be placed and how strings had to be grouped. 
It was quickly abandoned due to its inflexibility and poor results. This feature was the fresh start we needed to finally tackle this problem.

It takes care of all the shorcommings the previous attempt had
* It does stringing automatically.
* It places powerstations based on centers of mass of devices belonging to them.
* It doesn't rely on flat strings per device input, instead it groups devices based on multiple criteria like a DC/AC ratio range,
  azimuth, corridors, shapes of the selected areas, frame capacity, AC power of transformers or central inverters.

Here are some videos demonstrating the capabilities of the new algorithm:

<details open>
<summary><strong>Quick execution for massive parks</strong></summary>
<video width="100%" preload="metadata" muted controls loop>
    <source src="/assets/huge_park.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
</details>

