# Scanning-Local-Network
Scanning Local Network for Open Ports
** Scanning of local Networks for open ports **

*Overview*
This project performs a TCP SYN scan on the local network using Nmap to discover active devices, their IP addresses, and open ports. It includes optional packet inspection using Wireshark and a brief analysis of potential security risks.

a)NMAP was installed into the system.

b)local IP range was extracted through Windows terminal with Command "ipconfig"
  (which is provided in attached Screenshots respectively)

c)To run and perform TCP SYN scan we have to know range 
 for eg.- if IP = 192.168.1.10 and subnet = 255.255.255.0, range is 192.168.1.0/24.

d)Performing TCP SYN scan on NMAP with the range 192.168.130.0/24
 report was given : Nmap scan report for 192.168.130.81
Host is up (0.00055s latency).
Not shown: 997 closed tcp ports (reset)
PORT    STATE SERVICE
135/tcp open  msrpc
139/tcp open  netbios-ssn
445/tcp open  microsoft-ds

e) using WIRESHARK i found some interesting ports to be Scanned
(provided some screenshots of what i have found on wireshark)
using some filters such as.- tcp.port == 80

f) research on common services running on selected ports-

Port	Service	Description
22	SSH	Secure Shell
80	HTTP	Web Server
443	HTTPS	Secure Web
3389	RDP	Windows Remote Desktop

e)Potential risks causes by open ports are-

1.Unnecessary open ports = risk.
2.Remote desktop (3389) open? Might be exposed to brute-force.
3.FTP (21) without TLS? Vulnerable to credential sniffing.
4.IoT devices often expose telnet or insecure web interfaces.
