# Shell
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

# Reference
[LINUX SHELL PROGRAMMING : SPECIAL VARIABLES][SV]


[SV]: <https://www.bogotobogo.com/Linux/linux_shell_programming_tutorial3_special_variables.php>
