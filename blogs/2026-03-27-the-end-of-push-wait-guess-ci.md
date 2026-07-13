---
title: "The end of push-wait-guess CI"
url: "https://depot.dev/blog/the-end-of-push-wait-guess-ci"
date: "2026-03-27"
author: ""
feed_url: "https://depot.dev/rss.xml"
---
The old CI debugging loop goes: edit YAML, commit, push, wait, squint at logs, repeat. Depot CI replaces that with a local loop you can actually control, from running workflows against uncommitted changes to SSHing into the runner mid-job.
