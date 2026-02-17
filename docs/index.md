# Introduction

!!! abstract "Business Continuity and Disaster Recovery"

Modern disk systems can be made very reliable. It is assumed you have previously covered RAID, clustering, volume copy, mirroring, distributed file systems, encoding, erasure coding. Single points of failure are eliminated in modern storage systems. A common fallacy is to assume that resilience and high availability is the same thing as a backup; it is not. 

1. People make mistakes and inadvertently destroy storage systems.
2. Malicious actors may do the same.
3. Ransomware has been a very significant cause of data loss; other forms of malware may also be.
4. Physical incidents may occur; fire and floods are common in Ireland, other forms of disasters in other countries.
5. Grid failures combined with the failure of backup power may cause power loss events.
6. Physical equipment failure in a data centre may cause catastrophic damage.

Every business should have a clear _data retention policy_ which is compliant with legislative and governance requirements including GDPR, backups must be compliant with this policy. Things can go badly wrong if this is not the case.   



