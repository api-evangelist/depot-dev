---
title: "How simulations reduce the guesswork in our infrastructure decisions"
url: "https://depot.dev/blog/how-simulations-reduce-guesswork"
date: "2026-02-26"
feed_url: "https://depot.dev/rss.xml"
---
We had a standby pool algorithm with over a dozen tunable parameters and no good way to test changes without risking real customer latency. So we built a simulator fed with real job data, ran hyperparameter optimization on it, and found a configuration that was faster and cheaper.
