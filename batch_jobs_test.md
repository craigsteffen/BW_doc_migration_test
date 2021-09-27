##Batch Jobs
Users must submit jobs to the queue in batch mode for normal job runs.

Example scripts are in /sw/userdoc/samplescripts.  A hybrid xe+xk script is also located there showing how to request nodes of both types (xe_xk.pbs ).

If you're using PrgEnv-intel with OpenMP, please see https://bluewaters.ncsa.illinois.edu/intel-compiler for specific recommendations regarding aprun and setting KMP_AFFINITY appropriately.

XE nodes only, packing 1 MPI task per integer core (2 per bulldozer core)

`#!/bin/bash
#IMPORTANT! If above shell isn't the same as your account default shell, add
# the "-i" option to the above line to be able to use "module" commands. 

### set the number of nodes
### set the number of PEs per node
#PBS -l nodes=2048:ppn=32:xe
`

