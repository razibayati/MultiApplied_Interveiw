# MultiApplied_Interveiw
Create a flow tracking application using a raw socket (SOCK_RAW). The program needs to function on a Linux operating system. The application must perform the following tasks:

•	Open a raw network socket (SOCK_RAW)

•	Set it up to only receive IPv4 packets on a physical interface given as the first argument to the program

•	For each packet received, parse the following values:

o	IP source

o	IP destination

o	IP protocol

o	source UDP/TCP port (if protocol is UDP or TCP)

o	destination UDP/TCP port (if protocol is UDP or TCP)

•	Counts the number of packets received per combination of values

•	Every 10 seconds, print the counts of each packet flow to standard out in a human-readable form

example output, note that you don't need to match this formatting exactly its just an example of how you could showcase all the details:

#python3 sniffer.py enp1s0

10.100.50.151:34164<->255.255.255.255:10001 17 => 8

10.87.0.1<->224.0.0.5 89 => 1

10.87.100.151:1194<->10.87.100.5:1194 17 => 16

10.87.100.162:50956<->10.250.0.1:8003 6 => 2

10.87.100.1<->10.87.100.5 1 => 4

10.87.100.1<->10.87.100.61 1 => 4

10.87.100.204:50922<->10.87.100.51:2005 17 => 39

10.87.100.205:52649<->10.87.100.51:2000 17 => 32

10.87.100.2:41890<->3.208.72.74:443 6 => 4

10.87.100.51:2000<->10.87.100.205:52649 17 => 32

10.87.100.51:2005<->10.87.100.204:50922 17 => 41

10.87.100.52<->10.87.100.61 50 => 4

10.87.100.52<->10.87.100.63 47 => 2

10.87.100.5:1194<->10.87.100.151:1194 17 => 10

10.87.100.61<->10.0.1.6 47 => 2

10.87.100.61<->10.87.100.52 50 => 2

10.87.20.80:5404<->239.255.1.1:5405 17 => 2

10.87.21.80:5404<->239.255.1.2:5405 17 => 2


The program should be written in Python, without relying on libraries outside of the standard library.

