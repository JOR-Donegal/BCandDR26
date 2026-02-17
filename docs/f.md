# Disaster Recovery
Disaster Recovery or DR is required when a major incident creates a requirement to recreate the infrastructure and data of a site. In Ireland, this will be after a fire or a flood. In other countries, it may be required after a tsunami, earthquake, volcano, military, or paramilitary incident. There is an entire topic to be looked at here called Business Continuity Management or BCM. Some backups must be kept off-site to facilitate DR and the requirements here may be complex. In modern systems, we will try to have off-site replication, such that a failure on the main site may cause zero downtime. Large companies will have requirements for DR; for example, no DR site can be within 100kms of the primary site. Small sites may have a simpler system, where the weekly tapes go offsite to a data safe.

In disaster recovery planning, we look at scenarios where our main site may not longer be accessible or even in existence. Think about Fukashima, Chernobyl, the tsunami event of 2004, etc.

A cold site is a backup location which is not ready to go and may be in one of several states.
- It may have no equipment.
- It may have limited equipment.
- It may have equipment in a powered down or unconfigured state. 

A hot site is a site that is ready to go. It has equipment fully operational and just needs a copy of current backups, VMs etc. to go live. A dedicated hot site is a very expensive contingency.  

