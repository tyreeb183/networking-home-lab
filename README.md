\# Networking Home Lab — TCP/IP, DNS, DHCP \& Troubleshooting



\## Project Overview



This project demonstrates hands-on networking configuration, testing, and troubleshooting using Windows PowerShell.



The purpose of this home lab is to develop practical skills in TCP/IP networking, IP addressing, DNS, DHCP, subnetting, connectivity testing, and network diagnostics.



\## Technologies and Tools Used



\- Windows 11

\- Windows PowerShell

\- TCP/IP

\- IPv4 and IPv6

\- DNS (Domain Name System)

\- DHCP (Dynamic Host Configuration Protocol)

\- ICMP (Internet Control Message Protocol)

\- Network troubleshooting utilities

\- GitHub



\## Project Objectives



1\. Identify local IP addresses and network configurations.

2\. Verify connectivity to a local router.

3\. Test connectivity to an external internet address.

4\. Perform DNS lookups.

5\. Trace network routes.

6\. Test TCP port connectivity.

7\. Inspect DHCP configuration.

8\. Identify subnet masks and calculate usable IP ranges.

9\. Document troubleshooting commands and results.



\## Lab 1: IP Address Configuration



\*\*Command:\*\* `ipconfig`



Identified the following network settings:



\- IPv4 Address: 10.0.0.89

\- Subnet Mask: 255.255.255.0

\- Default Gateway: 10.0.0.1



\*\*Result:\*\* Successfully identified the laptop's private IPv4 address, subnet mask, and default gateway.



\## Lab 2: Local Network Connectivity



\*\*Command:\*\* `ping 10.0.0.1`



Tested communication between the laptop and the local router.



\*\*Results:\*\*



\- Packets sent: 4

\- Packets received: 4

\- Packet loss: 0%

\- Average response time: 5 ms



\*\*Conclusion:\*\* The router successfully responded to all four ICMP echo requests.



\## Lab 3: Internet Connectivity



\*\*Command:\*\* `ping 1.1.1.1`



Tested connectivity to Cloudflare's public IP address.



\*\*Results:\*\*



\- Packets sent: 4

\- Packets received: 4

\- Packet loss: 0%

\- Average response time: 22 ms



\*\*Conclusion:\*\* Successfully established IP connectivity beyond the local network.



\## Lab 4: DNS Troubleshooting



\*\*Command:\*\* `nslookup google.com`



Performed a DNS lookup to identify the IP addresses associated with Google's domain.



\*\*Results:\*\*



\- DNS server: cdns01.comcast.net

\- Domain queried: google.com

\- IPv4 address returned: 142.250.190.238

\- IPv6 address returned: 2607:f8b0:4006:80f::200e



\*\*Conclusion:\*\* DNS resolution completed successfully and returned both IPv4 and IPv6 addresses.



\## Lab 5: Network Route Tracing



\*\*Command:\*\* `tracert 1.1.1.1`



Examined the network path between the laptop and Cloudflare.



\*\*Results:\*\*



\- Destination: 1.1.1.1

\- First hop: 10.0.0.1

\- Destination reached at hop 12

\- One intermediate hop did not respond to traceroute probes



\*\*Conclusion:\*\* Successfully traced the route to the destination. The intermediate timeout did not prevent the trace from completing.



\## Lab 6: TCP Port Connectivity



\*\*Command:\*\* `Test-NetConnection google.com -Port 443`



Tested TCP connectivity to Google's HTTPS service.



\*\*Results:\*\*



\- Destination: google.com

\- Port: 443

\- Protocol: TCP

\- TcpTestSucceeded: True



\*\*Conclusion:\*\* Successfully established a TCP connection to port 443.



\## Lab 7: DHCP Configuration



\*\*Command:\*\* `ipconfig /all`



Reviewed the laptop's automatic network configuration.



\*\*Results:\*\*



\- DHCP Enabled: Yes

\- DHCP Server: 10.0.0.1

\- Assigned IPv4 Address: 10.0.0.89

\- Default Gateway: 10.0.0.1



\*\*Conclusion:\*\* Verified that DHCP is enabled and the router supplies automatic IPv4 network configuration.



\## Lab 8: IPv4 Subnetting



\*\*Command:\*\* `Get-NetIPAddress -InterfaceAlias "Wi-Fi" -AddressFamily IPv4 | Select-Object IPAddress,PrefixLength`



\*\*Results:\*\*



\- IP Address: 10.0.0.89

\- Prefix Length: /24

\- Subnet Mask: 255.255.255.0

\- Network Address: 10.0.0.0

\- Broadcast Address: 10.0.0.255

\- Usable Host Range: 10.0.0.1 – 10.0.0.254

\- Usable Host Addresses: 254



\*\*Conclusion:\*\* Verified the configured IPv4 prefix and calculated the subnet's usable host range.



\## Network Troubleshooting Methodology



This project followed a basic network troubleshooting process:



1\. Examine the network adapter and IP configuration.

2\. Verify local router connectivity.

3\. Test external IP connectivity.

4\. Check DNS resolution.

5\. Trace the route to an external destination.

6\. Test connectivity to a specific TCP service.

7\. Verify DHCP and subnet configuration.



This approach helps distinguish local connectivity, routing, name resolution, and service connection issues.



\## Skills Demonstrated



\- Network configuration analysis

\- IPv4 addressing and subnetting

\- DHCP configuration inspection

\- DNS troubleshooting

\- ICMP ping testing

\- Network route tracing

\- TCP port connectivity testing

\- Windows PowerShell

\- Technical documentation

\- Basic network diagnostic methodology



\## Project Results



Successfully completed eight networking exercises using Windows PowerShell.



Verified local and external connectivity, successful DNS resolution, route tracing, TCP port connectivity, DHCP configuration, and IPv4 subnet settings.



\## Screenshots



Screenshots of the network diagnostic commands and results will be added later.



Sensitive device identifiers, including MAC addresses and DHCP client identifiers, will be hidden before publishing screenshots.



\## Future Improvements



\- Practice subnetting with additional network sizes.

\- Use Wireshark to analyze packets.

\- Explore DNS troubleshooting failures.

\- Build a virtual network using multiple devices.

\- Practice VLANs and routing with Cisco Packet Tracer.

\- Explore basic network security and firewall rules.



\## Conclusion



This Networking Home Lab demonstrates foundational networking knowledge and hands-on troubleshooting skills relevant to IT support, help desk, and entry-level networking positions.



