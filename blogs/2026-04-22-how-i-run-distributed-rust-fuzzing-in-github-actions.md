---
title: "How I run distributed Rust fuzzing in GitHub Actions"
url: "https://depot.dev/blog/distributed-rust-fuzzing"
date: "2026-04-22"
author: ""
feed_url: "https://depot.dev/rss.xml"
---
With agents writing the initial fuzz harness, the hardest part of getting fuzzing into CI is basically gone. This is the setup I landed on: cargo fuzz, a GitHub Actions matrix job to fan work across multiple runners, and Actions cache to keep the corpus growing between runs.
