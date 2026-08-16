---
title: "Why I reimplemented LVM (with worse guarantees)"
url: "https://depot.dev/blog/why-i-reimplemented-lvm"
date: "2026-08-13"
feed_url: "https://depot.dev/rss.xml"
---
Our microVMs launch in under a second, and assembling their block devices in parallel put LVM's roughly 100ms volume group-wide lock directly in the critical path. We kept the kernel's device-mapper, wrote our own control plane and gave up crash safety our ephemeral workloads never needed, making allocation roughly 100x faster.
