---
title: "Speed up CI by running independent steps in parallel"
url: "https://depot.dev/blog/independent-steps-in-parallel"
date: "2026-05-26"
author: ""
feed_url: "https://depot.dev/rss.xml"
---
Most CI jobs run as one long serial script even when half the work doesn't depend on the other half. You can run independent steps in parallel for faster CI. We'll compare two ways to do it: shell backgrounding and Depot CI's parallel steps.
