---
title: "Auth Log Analyzer"
summary: "A Python script that parses Linux auth logs, flags brute-force attempts, and summarizes the top offending IPs."
tools: [Python, Linux]
featured: true
order: 2
---
<!-- This is a sample project. Replace it with something you've built, or delete it. -->

## Problem

Reading `/var/log/auth.log` by hand to spot SSH brute-force attempts is slow.

## Approach

```python
import re
from collections import Counter

failed = re.compile(r"Failed password for .* from (\d+\.\d+\.\d+\.\d+)")
with open("auth.log") as f:
    hits = Counter(m.group(1) for line in f if (m := failed.search(line)))

for ip, count in hits.most_common(10):
    print(f"{ip:15} {count}")
```

## Results

Turned a manual review into a one-line command, and taught me regular
expressions along the way.
