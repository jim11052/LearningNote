### netcat 
netcat is a simple unix utility which reads and writes data across network connections, using TCP or UDP protocol.
#### nc \[-options\] hostname port\[s\] \[ports\] 
| Variable | Description |
| ------ | ------ |
| -z | zero-I/O mode \[used for scanning\] |
| -v | verbose \[use twice to be more verbose\] |
| -w secs | timeout for connects and final net reads |

- test connection
```sh
nc -zvw 10 8.8..8 53 
```

sudo tcpdump host 172.31.40.114 -w 1a.pcap

wireshark filter tcp.flags.syn==1 and ip.addr==172.31.40.114
"tcp.flags==0x12" looks for SYN/ACK packets (you could also use "tcp.flags.syn==1 and tcp.flags.ack==1", or, if you want SYN and SYN/ACK, use "tcp.flags.syn==1 or (tcp.flags.syn==1 and tcp.flags.ack==1)".
