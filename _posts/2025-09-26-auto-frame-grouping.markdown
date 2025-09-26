---
layout: post
title:  "Auto grouping frames for powerstations"
date:   2025-09-26 16:11:09 +0300
categories: Frame grouping
---

We had a friction point that our users have been facing for a long time: grouping frames manually is tedious and time-consuming.
So I've designed and implemented an algorithm that automatically groups frames for power stations based on multiple criteria like a DC/AC ratio range,
azimuth, corridors, shape of the areas, frame capacity, AC power of transformers or central inverters. Then it places power stations such that the amount of needed cabling is minimized.

Our next big milestone is to fully automate the design of solar parks, and this algorithm is a significant step towards that goal.
I've designed it so that it would be easy to extend and adapt to new requirements in the future as it is capable of grouping anything that has a capacity.
As of now it groups frames for power stations, but to enable fully automatic generation it will need to group strings for inverters.

Here are some videos demonstrating the capabilities of the new algorithm:

<details open>
<summary><strong>Quick execution for massive parks</strong></summary>
<video width="100%" preload="metadata" muted controls loop>
    <source src="/assets/huge_park.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
</details>

<details>
<summary><strong>Support for multiple frame presets per single area</strong></summary>
<video width="100%" preload="metadata" muted controls loop>
    <source src="/assets/multi_presets.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
</details>

<details>
<summary><strong>Group shape correlates with the Azimuth (rotation) of the frames</strong></summary>
<video width="100%" preload="metadata" muted controls loop>
    <source src="/assets/azimuth.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
</details>

<details>
<summary><strong>Multiple selection</strong></summary>
<video width="100%" preload="metadata" muted controls loop>
    <source src="/assets/multi_selection.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
</details>

<details>
<summary><strong>Custom block reference</strong></summary>
<video width="100%" preload="metadata" muted controls loop>
    <source src="/assets/blockreference.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
</details>
