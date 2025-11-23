---
layout: post
title:  "Single Line Diagram"
date:   2022-12-12 16:11:09 +0300
categories: Single Line Diagram
---

**Result**: Users having a visual representation of their electrical device tree directly in the drawing.

231 Monthly active users on average, 814 SLD generations per month on average.

**Involvement**: Full ownership.

Users needed a way to represent their schema for electrical design. It needed to support all system types and contain 
all cabling lengths. I've created a mechanism that recursively traverses the electrical component tree and draws each 
electrical entity starting from the lowest one. Over time the feature was expanded to include support for batteries, 
a detailed central inverter representation and other new requirements.

![Single line diagram with trunks]({{ site.baseurl }}/assets/sld_trunk.png)

<summary><strong>Single line diagram generation example</strong></summary>
<video width="100%" preload="metadata" muted controls loop>
    <source src="/assets/sld.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
