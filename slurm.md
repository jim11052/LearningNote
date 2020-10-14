# Slurm

 - https://slurm.schedmd.com/SLUG19/Priority_and_Fair_Trees.pdf
 - https://slurm.schedmd.com/slurm_ug_2011/Basic_Configuration_Usage.pdf
 - https://slurm.schedmd.com/reservations.html
 - https://slurm.schedmd.com/SLUG16/FederatedScheduling.pdf
 - https://slurm.schedmd.com/federation.html
 - https://slurm.schedmd.com/sprio.html
## squeue 
```sh
$ squeue --format='%.18i %.9P %.20j %.8u %.2t %.10M %.6D %R %x %Q %y' --sort=-Q
```

## sacctmgr
#### Add account and user 
```sh
$ sacctmgr -i add account [account_name] description=[account description] Organization=[organization]
$ sacctmgr -i create user [user_name] account=[account_name] adminlevel=None
```
#### QOS
```sh
# show slurm accounting qos
$ sacctmgr show qos format=name,MaxJobsAccruePerAccount,MaxSubmitJobsPerAccount
# modify slurm accounting qos (ex: qos name = normal)
$ sacctmgr modify qos [qos name] set MaxJobsAccruePerAccount=[number]
```
## Slurm Upgrade to 19.05.7
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
