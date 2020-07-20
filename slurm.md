# Slurm
## sacctmgr

### QOS
```sh
#show slurm accounting qos
$ sacctmgr show qos format=name,MaxJobsAccruePerAccount,MaxSubmitJobsPerAccount
#modify slurm accounting qos
$ sacctmgr modify qos [qos name] set MaxJobsAccruePerAccount=[number]
```

# Reference
[Slurm Workload Manager]: <https://slurm.schedmd.com/documentation.html>
