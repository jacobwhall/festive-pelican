# festive-pelican

A lil python package to make dask easier on the W&M HPC

## How to use

This package currently provides two functions that take the same arguments: `hpc_dask_cluster` and `hpc_dask_cluster`.
The former returns a [dask_jobqueue `PBSCluster`](https://jobqueue.dask.org/en/latest/generated/dask_jobqueue.PBSCluster.html), and the latter returns a [Prefect `DaskTaskRunner`](https://prefecthq.github.io/prefect-dask/#running-tasks-on-dask).

Here are the arguments these functions take:

```
num_procs: int,                        # number of processes you'd like
job_name: str,                         # name of PBS job
cluster: str,                          # name of cluster, right now this can just be "vortex"
cores_per_process: Optional[int]=None, # automatically scale 
walltime: str = "01:00:00",            # walltime of PBS job
**kwargs                               # anything else you'd like to pass to PBSCluster
```

## License

This project is licensed under GPLv3 or any later version.
See LICENSE.md for more information.
