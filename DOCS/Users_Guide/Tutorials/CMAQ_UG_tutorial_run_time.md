## CMAQ Tutorial 
### Strategies to Improve CMAQ Model Runtime 
Purpose: This tutorial shares common options and strategies that CMAQ developers recommend for improving model runtimes on common systems.


------------
#### Linux Environment Settings

```
limit stacksize unlimited 
```
#### Run time Process Configuration Settings

For these two variable, n should be >= m and m and n should be as close as SQRT(m*n) as possible.

   @ NPCOL  = m; @ NPROW =  n


#### HPC Queue Manager Options

One consideration is to reserve the entire node that CMAQ is running on so that the simulation can make use of maximum resources. In the SLURM queue manager, you can use the following option.
```
#SBATCH --exclusive
```



