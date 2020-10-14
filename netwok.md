### netcat 
netcat is a simple unix utility which reads and writes data across network connections, using TCP or UDP protocol.
#### nc \[-options\] hostname port\[s\] \[ports\] 

| Variable | Description |
| ------ | ------ |
| -z | zero-I/O mode \[used for scanning\] |
| -v | verbose \[use twice to be more verbose\] |
| -w secs | timeout for connects and final net reads |

```sh
nc -zvw 10 8.8..8 53 
```
### tcpdump 
dump traffic on a network

| Variable | Description |
| ------ | ------ |
| -w | Write the raw packets to file rather than parsing and printing them out |
| -v | verbose \[use twice to be more verbose\] |
| -w secs | timeout for connects and final net reads |

```sh
tcpdump host \[`hostname or ip`\] -w `file.pcap`
```
### wireshark filter
`tcp.flags==0x12` looks for SYN/ACK packets (you could also use `tcp.flags.syn==1 and tcp.flags.ack==1`, or, if you want SYN and SYN/ACK, use `tcp.flags.syn==1 or (tcp.flags.syn==1 and tcp.flags.ack==1)`.
- tcp.flags.syn==1 and ip.addr==`ip address`

