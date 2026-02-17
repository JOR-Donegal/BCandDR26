# Backup Architecture
Backup is complicated and normally requires the use of specialized software. Backup client software sits on a system which has access to data sets for backup and is responsible for forwarding data to the backup server, which has access to the backing storage to be used for backup and recovery. There are very many different arrangements of server and backing store/media server where the backup data will be kept. There must also be a repository of meta-data about the backups; what was backed up, when, on what media, this may also originate with the client but will be stored at the server.

- Backing stores may be of many different types.
- Tape has been used for +50 years, it is linear and sequential. It is still the cheapest way to store large capacities over long time periods.
- Disk may be used in tape emulation mode and is now the most normal way to do initial backup.
- Disks can be used in an array for performance.
- Customized storage systems with deduplication
- Cloud storage, such as Amazon Glacier

Backups are normally scheduled and for typical office applications, will be run after closing hours.
An SME might backup directly to tape after hours. For larger operations, backup will be to disk during a backup window and to tape or cloud at some point afterwards.

Systems which are always on are much more complex to plan. A partition might be snapshotted to allow for a stable copy to be taken. It could be mirrored to a different location and the backup taken of the mirror.

In the event of a physical incident like a fire, there is little point looking for a backup in the adjacent cabinet. Remote backup can be performed site-to-site and this reduces the risk of simultaneously losing both the system and its backups. Alternatively, where the customer has only one site, we install the backup system as far away as possible. In the University, Letterkenny Campus, backup to disk occurs at the CO-LAB, in the far south east corner of the site, over 300m away from the data centres it provides backup for.

For an SME, backup tapes should be kept in a proper fireproof media safe off site. Many business owners install the media safe at home.