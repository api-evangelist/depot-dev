---
title: "Improving system safety with Temporal Logic of Actions (TLA+)"
url: "https://depot.dev/blog/tla-verification"
date: "2026-07-20"
feed_url: "https://depot.dev/rss.xml"
---
Formal verification never seemed worth it: writing a faithful TLA+ spec took too long. But now agents can write the spec from your code. We tried it on the rebuilt Depot Registry garbage collector, and the model checker found something our tests and reviews didn't: a race that could delete live data.
