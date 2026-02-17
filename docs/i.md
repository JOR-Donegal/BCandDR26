# Bare-metal recovery

Backup of application servers and workstations, sometimes called bare-metal recovery, is a hard issue to resolve. Building a server may be a complex job, taking many days and specialist skills. Bespoke software and configuration may have been performed, there may be unique licenses and keys. Whenever we audit a site, we find these little snowflakes, unique servers and workstations which no one knows ho configured or when and no one has the information to rebuild. 

Identifying these problem devices is the first step, but properly making these devices recoverable is a difficult problem to solve. One temporary mitigation is to perform a P2V, a _physical to virtual conversion_ where we copy the contents of a physical machine to a VM. In most modern applications, we build the servers as VMs, backup and recovery become a very easy task. 

Procedures are important. 

One way of avoiding this problem is to ensure a server build record is created for each critical server. In an SME, this would be a file/box with instructions and copies of the media used. In a data centre, it’s the build documentation or scripts for a VM or class of VMs.    