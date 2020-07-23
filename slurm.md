# Slurm
## sacctmgr

#### QOS
```sh
# show slurm accounting qos
$ sacctmgr show qos format=name,MaxJobsAccruePerAccount,MaxSubmitJobsPerAccount
# modify slurm accounting qos (ex: qos name = normal)
$ sacctmgr modify qos [qos name] set MaxJobsAccruePerAccount=[number]
```
# Slurm Upgrade to 19.05.7
```sh
$ systemctl stop slurmd
$ cd tmp
$ wget https://download.schedmd.com/slurm/slurm-19.05.7.tar.bz2
$ tar -jvxf slurm-19.05.7.tar.bz2
$ cd slurm-19.05.7
$ ./configure --prefix=/usr 
$ make 
$ make install

$systemctl restart munge
$systemctl restart slurmd
```

# Reference
[Slurm Workload Manager][SWM]





[SWM]: <https://slurm.schedmd.com/documentation.html>
