# Argo energy analysis – from 06/03/2020 to 13/03/2020

## Introduction
We activated energy recording plugin in Slurm which is called the RAPL. RAPL measures energy for CPU and DRAM only.  The period of measurement was approximately a week starting from 06/03/2020 to 13/03/2020. Argo is a heterogeneous cluster with nodes from different architectural family.  When we configured the monitoring tool, the nodes needed to be restarted and this somehow gave us the variable to use to measure the time when this was running.

Command used to get the `scontrol show node  -o `

## Energy 

### Node states
State of the cluster (Argo) when the statistics was acquired:
* We have 2 nodes (nehalem[01-02])were not collecting data at all.
* All other nodes recorded normal readings except
* The following nodes had additional reason attribute from the rest of the nodes in the cluster at the time of data extraction from Slurm

| Node Name        | State         | Reasons  |
| -------------    |:-------------:| --------:|
| Node103          | IDLE+DRAIN    | Node crashes frequently |
| Node93           | IDLE+DRAIN    |  openib RETRY EXCEEDED ERROR |
| Node109          | IDLE+DRAIN     |  batch job complete failure |
| Node132          | IDLE+DRAIN     |    HD problems |
| Node133          | IDLE+DRAIN      |    Low RealMemory |
| Node134          | IDLE+DRAIN      |    Error |
| Serial02         | DOWN+POWER      |    ResumeTimeout reached |
| Westmere01       | IDLE+DRAIN+POWER   |    Low RealMemory |


### Energy reading per partition 
The table 1.1 shows the consumed Mega-joules(Mj) per partition and the lowest-Kilo-joules (kj). It can be noted that CMSP partition uses most of the energy followed by the long partition and GPU partition having the lowest energy. In addition to that GPU nodes have high Lowestkilojoules considering that they are just 2 nodes which is expected.


## Classification per feature on a partition 


## Power 







