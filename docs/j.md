# SME Strategy
To finish I want to suggest a simple strategy for an SME. 

## Business Continuity
For business continuity I want to design a system where if a server fails, we can just keep on working on the same site. I'm going to presume that you've been able to consolidate services onto a single host server.

To begin, we set up a second identical host server. We split the critical services amongst the two hosts.

| Service     | Host1       | Host2   |
| ----------- | ----------- |---------|
| AAA| dc1 | dc2 |
| DNS | dc1 | dc2|
| DHCP | dc1 | dc2|
| File Sharing | fs1 | fs2|

Active directory synchronizes automatically and if you set the DCs up correctly, so does DNS and DHCP.

We can set the file servers up to synchronize using DFS and similar technologies (look it up!).

We could still lose an entire VM! So I will write a script such that each VM shuts down during the night and makes a copy of itself to the other host.

## Backups
I will supply a tape backup system (or two!) for each host. I need to design a backup strategy. I will also do a backup on the VMs, at a certain frequency.

## Disaster Recovery
Some of my tapes will go off site to a _data safe_. I will have a spare tape drive at that location, and an inexpensive server (Host 3). I will periodically test restores to this system.

## Making it work
It must be someones job to make sure this all works, define quality assurance for this, regular test!