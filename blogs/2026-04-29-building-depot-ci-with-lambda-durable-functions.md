---
title: "Building Depot CI with Lambda durable functions"
url: "https://depot.dev/blog/building-ci-with-durable-lambda"
date: "2026-04-29"
author: ""
feed_url: "https://depot.dev/rss.xml"
---
Depot CI's orchestrator runs on AWS Lambda durable functions. The orchestrator checkpoints state, suspends between events, and never burns compute while waiting. Here's how we designed the run-workflow-job hierarchy and the callback-driven orchestration loop that powers it.
