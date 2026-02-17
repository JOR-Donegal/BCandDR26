# Principles
Some analysis needs to be carried out to understand the characteristics of the most typical restores requested and the reason for them. Tapes may be too slow to use as a primary backup mechanism. On many sites we now do backup to disk during the _backup window_ and then backup to tape at our leisure; this process is known as _staging_ the backups. Other techniques exist to make this process efficient; volume copy, replication, cloning etc. Any system planning for backup should meet these typical requirements.

The _Recovery-Point Objective_ (RPO) is a point in time at which data should be recoverable after an incident. This defines the granularity of backups and the customer’s ability to tolerate data loss. If we backup at 2200 every evening, are we tolerating a full business day of potential data loss? If we want zero RPO, we need to mirror each change to a backup system which has versioning. For example, many Cloud solutions will back up in real-time and keep up to 30 copies of a document in a revision archive.

The _Recovery Time Objective_ (RTO) is the time it takes to reinstate data after an incident. It defines the customer’s ability to tolerate downtime or the unavailability of systems or data. RTO determines the kind of backup systems and media we can use.
Where the RTO is in days, we can restore from off-site backup tapes or to a cold recovery site.
To ensure an RTO of less than a day, we would need a hot recovery site.

To enable recovery in hours, we need to be able to recover from disk, not tape. There are exceptions, where complex tape robot systems are employed.

For shorter term recovery times, we are leaving the realm of pure backup/restore.

If I am spec’ing a backup system for an SME, I insist that the backups are formally checked, typically once a week. I had a site who asked me to recover their data from tape after a server failure, they had no IT contractor. When I examined the tape backup, I realized that the customer had the same tape in the drive for six months and it had worn out at some point. Data recovery…. six months out of date! The customer agreed to a proper maintenance contract after that, but too late for their data. I have far too many examples of that, where small businesses have had a a100% data loss. During the recent spate of ransomware infections, almost every business that contacted me after the event had a 100% data loss.

Backups are essential and so is the quality assurance, knowing that the backups work. In an SME, I specify that a test restore needs to be done once a week. It is the only way to be sure the backups are working.

With larger sites, the principle is the same, but the frequency and detail of checks will be different. In any DR exercise these processes will be procedural, complex, and thorough. The QA testing is a very effective way of ensuring that data recovery can take place, it is a good exercise to prepare for a real incident of potential data loss. Gaps are identified and mitigated, and the recovery team become familiar with the processes. 

In a data archive, _durability_ refers to the ability of stored data to remain intact, uncorrupted, and permanently preserved over long periods of time, even in the face of hardware failures, software errors, or environmental issues.