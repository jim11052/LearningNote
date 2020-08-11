tail -f remotelogs.log | perl -pe 's/(openvpn|ran)/\e[1;41m$&\e[0m/g'

# Shell
## Commomly used commands
### arp-scan 
The ARP scanner and can scan the duplicate ips on the local network
```sh
$ arp-scan --interface=eth0 --localnet
```

### rsync
A fast, versatile, remote (and local) file-copying tool
| Variable | Description |
| ------ | ------ |
| -P | Show progress during transfer, same as --partial --progress |
| -a | Archive mode. This is equivalent to -rlptgoD. It is a quick way of saying you want recursion and want to preserve almost everything, same as --archive |
| -v | This option increases the amount of information you are given during the transfer. 
| -e | This option allows you to choose an alternative remote shell program to use for communication between the local and remote copies of rsync. Typically, rsync        is configured to use ssh by default, but you may prefer to use rsh on a local network. 
| -r | This tells rsync to copy directories recursively, same as --recursive |
```sh
$ rsync -Pav -e "ssh -i $keypath username@hostname:/fromdir /todir
```


                          

### netstat
Print network connections, routing tables, interface statistics, masquerade connections, and multicast memberships
| Variable | Description |
| ------ | ------ |
| -t | TCP |
| -u | UDP |
| -l | Show only listening sockets. |
| -n | Unless the --numeric (-n) option is specified, the socket address is resolved to its canonical host name (FQDN), and the port number is translated into the          corresponding service name. |
| -p | Show the PID and name of the program to which each socket belongs. |
```sh
$ netstat -tulnp
```

## Shell Script useful special variables
| Variable | Description |
| ------ | ------ |
| $0 | The filename of the current script. |
| $n | These variables correspond to the arguments with which a script was invoked. Here n is a positive decimal number corresponding to the position of an argument (the first argument is $1, the second argument is $2, and so on). |
| $$ | The process ID of the current shell. For shell scripts, this is the process ID under which they are executing. |
| $# | The number of arguments supplied to a script. |
| $@ | All the arguments are individually double quoted. If a script receives two arguments, $@ is equivalent to $1 $2. |
| $* | All the arguments are double quoted. If a script receives two arguments, $* is equivalent to $1 $2. |
| $? | The exit status of the last command executed. |
| $! | The process ID of the last background command. |
| $_ | The last argument of the previous command |
| > /dev/null 2>&1 | `2` refers to the second file descriptor of the process, i.e. stderr.  `>` means redirection. `&1` means the target of the redirection should be the same location as the first file descriptor, i.e. stdout. |

# Bash color 
| Regular Colors |        | Bold       |        | Background |        |
| ------         | ------ | ------     | ------ | ------     | ------ |
| Value          | Color  | Value      | Color  | Value      | Color  |
| `\e[0;30m`     | Black  | `\e[1;30m` | Black  | `\e[40m`   | Black  |
| `\e[0;31m`     | Red    | `\e[1;31m` | Red    | `\e[41m`   | Red    |
| `\e[0;32m`     | Green  | `\e[1;32m` | Green  | `\e[42m`   | Green  |
| `\e[0;33m`     | Yellow | `\e[1;33m` | Yellow | `\e[43m`   | Yellow |
| `\e[0;34m`     | Blue   | `\e[1;34m` | Blue   | `\e[44m`   | Blue   |
| `\e[0;35m`     | Purple | `\e[1;35m` | Purple | `\e[45m`   | Purple |
| `\e[0;36m`     | Cyan   | `\e[1;36m` | Cyan   | `\e[46m`   | Cyan   |
| `\e[0;37m`     | White  | `\e[1;37m` | White  | `\e[47m`   | White  |


# Reference
[LINUX SHELL PROGRAMMING : SPECIAL VARIABLES][SV]


[SV]: <https://www.bogotobogo.com/Linux/linux_shell_programming_tutorial3_special_variables.php>
