## Paramiko
Paramiko is an SSH2 remote secure connection based on Python, which supports authentication and key methods. 
It can realize remote command execution, file transfer, intermediate SSH agent and other functions. 
Compared with Pexpect, the encapsulation level is higher.

### Establish ssh connection, execute remote command, file transfer
> ssh = paramiko.SSHClient()
> ssh.set_missing_host_key_policy(paramiko.MissingHostKeyPolicy())
> try:
>># connect remote host
>>ssh.connect(hostname=`hostname`, username=`username`, password=`password`, key_filename=`keyPath`, timeout='value')
>>     
>># transfer file
>>ftp_client = ssh.open_sftp()
>># from client to remote host
>>ftp_client.put(`file_local_path`, `file_remote_path`)
>># from remote host to cilent
>>sftp.get(`file_remote_path`, `file_local_path`)
>>ftp_client.close()
>>
>># execute remote command
>>ssh_stdin, ssh_stdout, ssh_stderr = ssh.exec_command(`command`)
>>ssh_stderr = ''.join(ssh_stderr.readlines())
>>
>># close connection
>>ssh.close() 
