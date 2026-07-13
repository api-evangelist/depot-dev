---
title: "Failure fingerprints: Comparing test failures over time"
url: "https://depot.dev/blog/failure-fingerprints"
date: "2026-07-02"
author: ""
feed_url: "https://depot.dev/rss.xml"
---
To make recurring test failures easier to reason about we needed to include historical context. Here's how we derive a stable identity for each test and a fingerprint for each failure, so you can tell a brand-new problem from the same flaky test you've seen a dozen times.
