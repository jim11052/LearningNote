sudo tcpdump host 172.31.40.114 -w 1a.pcap

wireshark filter tcp.flags.syn==1 and ip.addr==172.31.40.114
"tcp.flags==0x12" looks for SYN/ACK packets (you could also use "tcp.flags.syn==1 and tcp.flags.ack==1", or, if you want SYN and SYN/ACK, use "tcp.flags.syn==1 or (tcp.flags.syn==1 and tcp.flags.ack==1)".
