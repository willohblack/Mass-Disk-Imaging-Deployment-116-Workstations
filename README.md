**Mass Disk Imaging & OS Deployment — 116 Workstations**


Planned and executed a full-scale disk imaging and restore operation across a 116-computer lab using Rescuezilla, cutting deployment time by running multiple stations in parallel.


**Project Screenshots**

<img width="1365" height="768" alt="Gemini_Generated_Image_22rppi22rppi22rp" src="https://github.com/user-attachments/assets/ecfe9250-6400-4b7b-98c7-7fe0aa40cf1c" />

<img width="1365" height="768" alt="Gemini_Generated_Image_fcvr0tfcvr0tfcvr" src="https://github.com/user-attachments/assets/ec5330d0-a0d1-441c-a89a-54bc82b65f15" />



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

<img width="1365" height="768" alt="Gemini_Generated_Image_6v3b1h6v3b1h6v3b" src="https://github.com/user-attachments/assets/d650b5dc-4228-41f7-b0bd-9488180c4e8b" />

<img width="1365" height="768" alt="Gemini_Generated_Image_22rppi22rppi22rp" src="https://github.com/user-attachments/assets/018b7a6e-c1dc-45ef-8237-415edb024872" />


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

<img width="1195" height="896" alt="Gemini_Generated_Image_fz613xfz613xfz61" src="https://github.com/user-attachments/assets/50a0089a-7ee4-4875-a31d-8af651f5df31" />

<img width="1195" height="896" alt="Gemini_Generated_Image_fz613xfz613xfz61 (1)" src="https://github.com/user-attachments/assets/f4087556-3e43-4772-bf48-8bfcd852cf41" />

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
