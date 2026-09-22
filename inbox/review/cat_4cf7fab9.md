---
type: cat
id: cat_4cf7fab9
title: 'Show HN: Drop – A rootless Linux sandbox with gVisor support'
resource: https://droprun.sh/
t_confidence: 0.6499999999999999
t_relevance: 0.7
t_signal: 0.6
t_reading_minutes: 1
horizon: read-today
lane: tech
timestamp: 2026-09-22T17:00:37.6713601+00:00
published_at: 2026-09-22T13:52:47.0000000+00:00
excerpt: "I created Drop because I always felt uneasy installing and running third-party programs using my main user account. A single compromised dependency means a full compromise of the system. What is even worse, because I ship software from my computer, a single compromised dependency can lead to compromise of all the users of my software. Containers and VMs are one solution, but for local work, they are often detrimental to productivity. It takes effort to configure a machine with all the tools and configs needed for productive work, but a container or a VM will be stripped of all these tools. This is great for production deployments, where the aim is a reproducible system with minimal dependencies, but can get in the way of productive local work. Drop is language independent, but the workflow is inspired by Python's virtualenv. With virtualenv the environment isolation is only a convention that relies on installed dependencies being good citizens. With Drop the isolation is enforced. Each Drop environment gets its own writable and easily disposable home dir, with only selected config files and dirs from the original home mounted, mostly read-only. Drop uses Linux namespaces for isolation (user, mount, network, PID, IPC, cgroup), doesn't require root and, as an option, uses gVisor user-space kernel, which adds protection against exploiting host kernel vulnerabilities to escape the sandbox. I don't want to make the introductory post too lengthy, but I'm here to answer any questions and give any additional technical details. Note: This is my 3rd submission of the project, the first two did not draw attention. Since then I have added support for gVisor and created a project website to better explain the concept and organize documentation. Comments URL: https://news.ycombinator.com/item?id=49801329 Points: 92 # Comments: 27"
t_source: source_hn
author: mixedbit
t_suggested_tags:
- topic/docker
- topic/linux
- topic/python
- topic/typescript
...
---
## Summary

Summary: Show HN: Drop – A rootless Linux sandbox with gVisor support
