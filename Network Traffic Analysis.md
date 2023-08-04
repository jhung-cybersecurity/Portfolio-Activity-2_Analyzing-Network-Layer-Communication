# Prompt

You are a cybersecurity analyst working at a company that specializes in providing IT consultant services.
Several customers contacted your company to report that they were not able to access the company website www.yummyrecipesforme.com,
and saw the error “destination port unreachable” after waiting for the page to load. 

You are tasked with analyzing the situation and determining which network protocol was affected during this incident. To start, you visit the website and you also receive the error “destination port unreachable.” Next, you load your network analyzer tool, tcpdump, and load the webpage again. This time, you receive a lot of packets in your network analyzer. The analyzer shows that when you send UDP packets and receive an ICMP response returned to your host, the results contain an error message: “udp port 53 unreachable.”
 
# DNS & ICMP Traffic Log

13:24:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain: 35084+ A?
yummyrecipesforme.com. (24)  
13:24:36.098564 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2
udp port 53 unreachable length 254  

13:26:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain: 35084+ A?
yummyrecipesforme.com. (24)  
13:27:15.934126 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2
udp port 53 unreachable length 320  

13:28:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain: 35084+ A?
yummyrecipesforme.com. (24)  
13:28:50.022967 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2
udp port 53 unreachable length 150  

# Cybersecurity Incident Report: Network Traffic Analysis  

### Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log  

> Response:
> 
> The DNS & ICMP Traffic Log reveals that the DNS server is down and/or reachable. More specifically, the log states "udp port 53 unreachable". 


### Part 2: Explain your analysis of the data and provide one solution to implement.  

> Response:
> 
> The incident occurred in the afternoon around 1:24PM. Through the use of packet sniffing tests using tcpdump, the team was able to find that DNS port 53 was unreachable.
> This issue has been addressed to the managers. However, the team suspects that the domain is facing a DoS attack with the over flow of network traffic.
> 






