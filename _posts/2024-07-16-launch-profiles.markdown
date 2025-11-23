---
layout: post
title:  "Launch profiles"
date:   2024-07-16 16:11:09 +0300
categories: Devops
---

**Result**: We can launch AutoCAD and our plugin right after cloning the repo, without doing any changes, without any
changes to any local files.

**Involvement**: Full ownership.

At the time, to automatically launch our plugin from the IDE we need to edit lsp files in AutoCAD's directory.
This was not that good because we have multiple AutoCADs and it didn't work out of the box just after cloning the 
repository. Launch profiles solve that by launching a custom script from the repo. It runs the selected AutoCAD with 
some standard input arguments that tell it to run a lisp script. The lisp script tells AutoCAD to add the dll we build
to the trusted paths list and tells it to load the DLL.