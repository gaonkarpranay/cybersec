==**with nmap -sS -p- &lt;target&gt; ,The `-sS` option is a TCP-only scan because it relies on the TCP three-way handshake (SYN, SYN-ACK, ACK). UDP has no handshake, so `-sS` cannot be used for ports that running UDP services**==

![ec2899ebec69488e444d2b8a2bd8e530.png](../../../images/ec2899ebec69488e444d2b8a2bd8e530.png)

==**if a system is running a UDP service on a common port it willl be easily bypassed with the above command to identify the udp ports we have to specify -sU option ,Instead, Nmap sends a UDP datagram to each port and interprets the response.**==

&nbsp;

**running all http scripts on a taget with port 80 service detection and** **stealth scan**

==**![5d2c3888e9e81caa753fd54fdf7423be.png](../../../images/5d2c3888e9e81caa753fd54fdf7423be.png)![a33c5d446652464757bd7bc45be1f3b1.png](../../../images/a33c5d446652464757bd7bc45be1f3b1.png)**==

&nbsp;

==**scan all tcp ports using SYN and**==

==**![ff5da1ed5e673555bf045acd25b65dc4.png](../../../images/ff5da1ed5e673555bf045acd25b65dc4.png)**==

&nbsp;

==**scan all ports using UDP packets,,if a service is runnning on a udp port it will be not shown using -sS option**==

==**![73ebbe937b5c41ac32f79577cad6370b.png](../../../images/73ebbe937b5c41ac32f79577cad6370b.png)**==