---
layout: post
title:  "Slack Jira plugin for the support team"
date:   2025-08-20 16:11:09 +0300
categories: Devops
---

**Result**: Increased awareness of 'Awaiting for response' Jira tickets in the support team, leading to faster response times and improved customer satisfaction.

**Involvement**: Full ownership.

![Pinger Screenshot]({{ site.baseurl }}/assets/pinger.png)

Wrote a script in Powershell and created a Task Scheduler job that runs it every day in the morning. It takes in a Slack channel ID, a Jira JQL query as parameters.
It then queries Jira for issues matching the JQL query and posts a message in the specified Slack channel with a link to each issue found. During it's lifespan it
was running across four different Slack channels, for three different teams, each with its own JQL query.