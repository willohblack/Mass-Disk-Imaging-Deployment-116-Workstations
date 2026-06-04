**Mass Disk Imaging & OS Deployment — 116 Workstations**


Planned and executed a full-scale disk imaging and restore operation across a 116-computer lab using Rescuezilla, cutting deployment time by running multiple stations in parallel.


**Project Screenshots**

<img width="3200" height="1800" alt="dawood_lab_116_computers" src="https://github.com/user-attachments/assets/47161857-a88b-4332-a82c-516dae74c3eb" />
<img width="3200" height="2400" alt="rescuezilla_stations_restore" src="https://github.com/user-attachments/assets/72e4cfb3-12af-4c9b-9ec5-2383e601110a" />
<img width="3200" height="2400" alt="rescuezilla_partition_select" src="https://github.com/user-attachments/assets/2e7d44d1-5eea-4133-9134-f7ab70dcdcbd" />

**Project Overview**

FieldDetailsEnvironmentComputer lab — 116 Dell workstationsTool usedRescuezilla (bootable USB)MethodParallel restore — 3+ stations simultaneouslyOS image typeStandardised Windows imagePartition typesNTFS, BitLocker, vFAT, MS ReservedOutcome116/116 machines restored with zero data loss

**What Was Done**

**1. Master Image Creation**
Configured a reference Dell workstation to the required OS state
Created a full disk image using Rescuezilla and stored it on external storage

**2. Partition Identification**

Rescuezilla detected the following partition layout across connected drives:

#1   200MB   Drive 2, Partition 1: 200MB vfat

#2    16MB   Drive 2, Partition 2: 16MB MS_Reserved_Partition

#3   1.8TB   Drive 2, Partition 3: 1.8TB ntfs

#4  28.9GB   Drive 3, Partition 1: 28.9GB vfat  ← RESCUEZILLA image partition

#5   100MB   Drive 20, Partition 1: 100MB vfat

#6    16MB   Drive 20, Partition 2: 16MB MS_Reserved_Partition

#7  475.9GB  Drive 20, Partition 3: 475.9GB BitLocker

#8   911MB   Drive 20, Partition 4: 911MB ntfs


**3. Parallel Deployment**

Booted each workstation from USB into Rescuezilla
Ran simultaneous restores on 3+ machines at a time
Monitored progress bars and completed all 116 restores

**4. Verification**

Verified each machine booted successfully post-restore
Confirmed OS integrity and uniform configuration across all workstations
Documented the process for the IT team for future use


**Tools & Technologies**

Rescuezilla — open-source disk imaging and restore tool

Bootable USB — used as the boot medium on each workstation

Dell Workstations — target hardware across the lab

Partition Management — handled NTFS, BitLocker, vFAT, and MS Reserved partitions

Parallel Deployment — 3+ simultaneous restores to maximise efficiency


**Results**

MetricValueTotal workstations imaged116Stations run in parallel3+Data loss incidents0Estimated time saved vs. manual install~40+ hoursFinal stateAll machines uniform, booted, production-ready

**Repository Structure**

├── images/
│   ├── dawood_lab_116_computers.jpg
│   ├── rescuezilla_stations_restore.jpg
│   └── rescuezilla_partition_select.jpg
└── README.md

**Author**

Dawood
IT Technician · Cloud & Infrastructure Portfolio
Building hands-on AWS and on-premises IT solutions.

**License**

This project is documented for portfolio purposes. No source code is distributed.
