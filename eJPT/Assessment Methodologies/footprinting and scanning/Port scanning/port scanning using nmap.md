## no ping option (-Pn) consider the host as alive and scan most common 1000 ports (unless specified) must used scan while scanning a single target if -Pn is not specified it again scan for host discovery using ICMP packets 

![dc5a4fe7fd73f10502e5175d2ab01c9c.png](../../../images/dc5a4fe7fd73f10502e5175d2ab01c9c.png)

fast scan `nmap -Pn -F <target>`

![a5db2ce40ac79540b8895a9f58ae57b8.png](../../../images/a5db2ce40ac79540b8895a9f58ae57b8.png)

specific port scan `nmap -Pn -p 80,445`

![6c227689d28372c41b546c8d87551ecb.png](../../../images/6c227689d28372c41b546c8d87551ecb.png)

TCP conect scan:- completes a 3 way handshake connection

&nbsp;`nmap -Pn -sT <target>`

![e549b28bb95f527fc005dd08aad93fe7.png](../../../images/e549b28bb95f527fc005dd08aad93fe7.png)

![16ccd262a5be3fd7013445a6e161f0d1.png](../../../images/16ccd262a5be3fd7013445a6e161f0d1.png)

UDP port scan `nmap -Pn -sU <target>`

![96434e14c32f695518b265504bf23442.png](../../../images/96434e14c32f695518b265504bf23442.png)

### ==TCP SYN scan/Stealth scan/half-open scan(automatically runs when running through root privilages)==

### In  a SYN scan the nmap send s SYN packet to specific ports and waits  for the ports to reply with SYN-ACK if the host sends a SYN-ACK it means the prot is open ,when nmap receives a SYN-ACk packet it terminates the handshake by sending a RST packet .The process can be seen clearly in the below image.

![19b53c3f3240ff24ede433a675f14100.png](../../../images/19b53c3f3240ff24ede433a675f14100.png)![be9059f847d7b53a660ef7c65c9bf68b.png](../../../images/be9059f847d7b53a660ef7c65c9bf68b.png)

### A RST confirms that the port is actually closed,if it does not receives anything from host that means may be a firewall is hiding behind the host.because the firewall may be filtering the RST packets passing through the it from a host.

&nbsp;

&nbsp;