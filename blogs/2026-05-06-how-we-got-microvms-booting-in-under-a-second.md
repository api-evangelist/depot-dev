---
title: "How we got microVMs booting in under a second"
url: "https://depot.dev/blog/optimizing-microvm-boot-times"
date: "2026-05-06"
author: ""
feed_url: "https://depot.dev/rss.xml"
---
Depot CI's VM scheduler is just-in-time: no pre-warming, no warm pool of standby VMs. We stacked optimizations to get microVM cold boots from 7 to 9 seconds down to under a second, and this post walks through each one.
