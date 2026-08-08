---
title: "Why SOCI belongs in the build"
url: "https://depot.dev/blog/why-soci-belongs-in-the-build"
date: "2026-08-04"
feed_url: "https://depot.dev/rss.xml"
---
Most of a large container's startup goes to pulling and decompressing files it never reads to boot. SOCI makes the image seekable so the runtime loads only the bytes it needs, and Depot writes that index during the build, so the image can lazy-load the instant it's pushed.
