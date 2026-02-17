# Backup Granularity
Once we know what our requirements are in terms of RPO and RTO, we can decide on the granularity of our backups. A starting point for any data set is to ask:

- How much data do we have?
- How much new/changed data is there per hour/day/week?

_Full backups_ are a copy of a data set and are the easiest to take, the easiest to track and to recover lost data from. However, they are expensive in capacity and time taken as we are backing up all data, including that which has not changed recently.

More economical are _incremental backups_; these are backups of files which have changed since the last backup. This will be most complex to track, but it will be the most economical solution in terms of capacity and time taken. Restoring from an incremental backup requires access to the last full backup, plus all the incremental backups which have taken place since.

A compromise between the two strategies above are _differential_ or _cumulative backups_. These will be a backup of all files which have changed since the last full backup. Differential backups are less economical in storage space and time than incremental backups but are quicker to restore from and easy to track. Restoring from a differential backup requires access to the last full backup, and the most recent differential backup.

<figure>
<img src = "https://jor-donegal.github.io/BCandDR26/images/fig1.jpg">
<figcaption>Fig 1. Spreadsheet Model.</figcaption>
</figure>

A few minutes builds a simple spreadsheet for modelling this. The graph above shows requirements where the initial data capacity is 5GB and we are adding 1GB a day. The numbers were kept close together for presentation only. The advantage of a spreadsheet is that I can plug in numbers for a customer and get results, it makes scenario planning easier.

Modern systems also allow the concept of a _synthetic backup_, where incremental backups are used to update an off-line copy of a full backup, such that a single full backup is available. This makes restores quick and easy.