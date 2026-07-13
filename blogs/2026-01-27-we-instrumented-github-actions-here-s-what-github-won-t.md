---
title: "We instrumented GitHub Actions. Here's what GitHub won't show you."
url: "https://depot.dev/blog/we-instrumented-github-actions"
date: "2026-01-27"
feed_url: "https://depot.dev/rss.xml"
---
Optimizing GitHub Actions without telemetry is guesswork. We built CI telemetry into Depot to surface real metrics for every job, like CPU, memory, and logs. Here's how we wired it together with OpenTelemetry and scaled it with ClickHouse.
