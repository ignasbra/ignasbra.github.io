---
layout: post
title:  "Parallel harness generation"
date:   2025-06-03 16:11:09 +0300
categories: Harness
---

**Result**: Significantly fewer cables required for single axis trackers

![Trunk harness screenshot]({{ site.baseurl }}/assets/harness_saved_cabling.png)

**Involvement**: I was a technical owner for the effort. I manged stakeholders and their requirements and distributed
work among developers and QA. I've also implemented a large part of the feature.

![Harness screenshot]({{ site.baseurl }}/assets/harness_ui.png)

Parallel harnessing works by generating harness connector points next to each positive pole of the strings except for
the last one that belongs to the harness. They are connected sequentially along the row by DC extension cables, one by
one. Same goes for the negative string poles. Parameters like maximum strings per harness needed to be respected, along 
with other domain restrictions like not allowing the same harness to connect two different rows.

The feature involved:
* Understanding complex domain requirements
* Adding two new harnessing types
* Redesigning our harnessing mechanisms to allow for multiple harness connectors
* Exporting to Yield
* Redoing the UI
* Calculating the bill of materials
* Supporting all the existing system types
