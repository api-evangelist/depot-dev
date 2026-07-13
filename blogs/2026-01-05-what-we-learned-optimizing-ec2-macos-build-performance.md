---
title: "What we learned optimizing EC2 macOS build performance"
url: "https://depot.dev/blog/what-we-learned-optimizing-ec2-macos-build-performance"
date: "2026-01-05"
feed_url: "https://depot.dev/rss.xml"
---
We ran iOS builds across different EBS disk configurations on EC2 macOS instances to find the optimal setup. We discovered that simply throwing more IOPS at the problem doesn't work the way you'd expect.
