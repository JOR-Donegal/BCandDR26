# Terminology
Before we start, terminology again!

_Storage_ is where we are keeping data.
- For domestic use, a workstations disks. 
- On a server, a storage array. 
- In a data center, a dedicated storage device, like _Network Attached Storage_ (NAS) or a _Storage Area Network_ (SAN).

A _backup_ is the process of creating duplicate copies of data retained solely to allow for its recovery should it be lost, deleted, or corrupted. 
Live synchronizing to a cloud store is not a backup! 
The technology required for backups is dictated by the volume of data, the time available to backup, the stability/dynamics of the data, versioning of data, restore frequency characteristics, etc. 
In the 1990s, we could back up an organization's critical data of a tape.
By the 2000s, we were using tape libraries.
In this decade, backup is often to disk and then tape, or to disk and then cloud. The issues in using these solutions are complex. 
The simplest layer of protection in a business are the backups.

_Business Continuity_ (BC) is the ability of an organization to continue to operate in the event of a disruption. It involves plans, equipment and people. If a small fire occurs in a server room, what are the services that were provided from that room, and how do we put them operational again? Where is the data? Where do we get equipment to put those services back in operation? Where are the instructions to do all of this and who has been trained to do it? This is _Business Continuity Planning_ (BCP) and we can expect to need it periodically in any business.

A _Disaster_ is a more major event, _Disaster Recovery Planning_ (DRP) are the procedures to respond to such an event. 

_Risk Analysis_ is a complex process, it is is the process of 

- Identifying potential threats
- Assess how likely they are to occur (L)
- Evaluate the impact (I)
- Prioritize on this basis (L*I)
- Identify mitigation strategies in order of priority

This is done badly in most instances I have seen. _Qualitative Risk Analysis_ will use arbitrary judgement and categories (Low, Medium, High) to produce a model.

In specialist domains such as the automobile or aviation industry, more formal methods may be used. _Quantitative Risk Analysis_ uses numerical data to measure risk and potential losses.
