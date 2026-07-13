---
title: "Observing Lambda durable functions"
url: "https://depot.dev/blog/observing-lambda-durable-functions"
date: "2026-06-16"
author: ""
feed_url: "https://depot.dev/rss.xml"
---
Durable Lambda functions break most of the tracing assumptions you carry over from regular code. They replay from the top every time they wake, so spans get emitted twice, parent spans lose their children, and queue wait time hides in the gaps. Here's how we restored end-to-end visibility into Depot CI's durable functions.
