---
layout: post
title:  "Parallel harness generation"
date:   2025-08-20 16:11:09 +0300
categories: Harness
---

**Result**: GM release builds are 95% cheaper now.

**Involvement**: I did it alone, but I could draw inspiration from the solution our RoofMount product had.

We make two builds of our application: one for pre 2025 AutoCAD and one for 2025 and later due to breaking changes in the AutoCAD API. 
This causes our signing process to be two times more expensive, because each dll signed costs money.
The issue is further amplified by the fact that we have a lot of dlls in our application. Obviously, this needed attention, so I set out to fix it.

For merging ILRepack was used.
I needed to fix Dotfuscator issues, add explicit exclusions, to ensure that obfuscation doesn't break the front end part of the application. 
I needed to modify the installer to ensure that the merged dlls are correctly referenced and copied to the output folder.
The CI/CD pipelines needed to be modified to ensure that the unmerged dlls are deleted after the merge and the merged dlls are moved to the output folder.