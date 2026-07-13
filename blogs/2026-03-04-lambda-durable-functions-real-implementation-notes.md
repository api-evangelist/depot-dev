---
title: "Lambda durable functions: Real implementation notes"
url: "https://depot.dev/blog/lambda-durable-implementation"
date: "2026-03-04"
feed_url: "https://depot.dev/rss.xml"
---
AWS Lambda durable functions let you write long-running processes that survive crashes and suspend compute entirely while waiting for external events. Getting them right requires understanding how replay works and the distinct failure modes of durable functions. Here's what we've learned from running durable functions for real.
